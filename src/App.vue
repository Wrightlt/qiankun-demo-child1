<template>
  <div id="app1">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <p>this is child project</p>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" v-show="false"/> -->
    <router-view></router-view>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  }
}
</script>

<style>
#app1 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  border: 1px solid red;
}
</style>
