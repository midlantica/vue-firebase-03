<template>
  <div id="app">
    <img src="./assets/logo.png" width="100">
    <Navbar />
    <router-view/>
  </div>
</template>

<script>
  import Navbar from './components/Navbar.vue'
  export default {
  components: { Navbar },
    name: 'App'
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
