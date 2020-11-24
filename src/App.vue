<template>
  <div id="app">
    <h1>Share Via:</h1>
    <facebook :url="url" scale="3"></facebook>
    <viber :url="url" scale="3"></viber>
  </div>
</template>

<script>
import Facebook from "./components/Facebook.vue";
import Viber from "./components/Viber.vue";

export default {
  name: "app",
  components: {
    Facebook,
    Viber
  },
  data() {
    return {
      url: "https://github.com/Kaung-myat-paing",
    };
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

  #app > span {
    margin: 1em;
  }
</style>
