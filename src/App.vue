<template>
  <div id="app">
    <img src="./assets/logo.png" />
    <router-link to="/index">aaa</router-link>
    <div>
      <Index msg="网站名-待定" />
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
import Index from "./components/Index.vue";

export default {
  name: "app",
  components: {
    Index,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
