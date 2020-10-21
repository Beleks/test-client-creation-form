<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <div class="header">Созднаие клиента</div>
    <Form></Form>
  </div>
</template>

<script>
import Form from "./components/Form.vue";

export default {
  name: "App",
  components: {
    Form,
  },
};
</script>

<style lang="scss">
body {
  padding: 1em;
  margin: 0;
  background-color: rgb(231, 231, 231);
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: white;
  padding: 2em;
  border-radius: 10px;
  .header {
    font-size: 1.3rem;
    margin-bottom: 1em;
  }
}
</style>
