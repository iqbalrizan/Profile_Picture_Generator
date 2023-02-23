<template>
  <div id="app">
    <div>
    <h1>Profile Picture Generator</h1>
    <show-avatar></show-avatar>
  </div>
  </div>
</template>

<script>
import ShowAvatar from "./components/ShowAvatar.vue";


export default {
  name: 'App',
  components: {
    ShowAvatar,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  background-color: rgb(0, 199, 199);
}
</style>
