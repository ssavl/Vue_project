<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h4>Важная страница</h4>
    <h1>Стартовая страница</h1>
    <hr>

    <ArticleDetail />


  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import ArticleDetail from "../views/ArticleDetail";

export default {
  name: 'App',
  components: {
    ArticleDetail
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
  margin-top: 60px;
}
</style>
