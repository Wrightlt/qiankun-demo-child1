<template>
    <div>
        this is child1 about page
        ----user----: {{userInfo.user}}
    </div>
</template>

<script>
import actions from "@/shared/actions"

export default {
    name: 'About',
    data() {
        return {
            userInfo: {
                token: null,
                user: null
            }
        }
    },
    mounted() {
        // 注册观察者函数
    // onGlobalStateChange 第二个参数为 true，表示立即执行一次观察者函数
    actions.onGlobalStateChange(state => {
        const { token, user } = state
        // 获取用户信息
        this.userInfo = {
            token,
            user
        }

         // 未登录 - 返回主页
        if (!token) {
            this.$message.error("未检测到登录信息！");
            return this.$router.push("/");
        }
    }, true)
    }
}
</script>