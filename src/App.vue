<template>
  <div id="app">
    <Nav />
    <Main />
    <Form />
    <Footer />
  </div>
</template>

<script>
import Main from "./components/Main.vue";
import Form from "./components/Form.vue";
import Nav from "./components/Nav.vue";

export default {
  name: "App",
  components: {
    Nav,
    Main,
    Form
  }
};
</script>

<style>
h1,
h2,
h3,
p {
  font-family: "Lato", sans-serif;
  color: white;
}
</style>
