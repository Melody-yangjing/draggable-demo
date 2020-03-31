<template>
  <div id="app">
    <hello></hello>
  </div>
</template>

<script>
import Hello from "./components/Hello";

export default {
  name: "app",
  components: {
    Hello
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 100%;
  height: 300px;
}

#app .logo {
  text-align: center;
}
</style>
