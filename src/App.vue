<template>
  <div>
    <NavbarComponents />
    <ProdutoFormComponent />
    <!-- <img src="./assets/logo.png" class="" /> -->
  </div>
</template>

<script>
import NavbarComponents from "./components/NavBar.vue";
import ProdutoFormComponent from "./components/produto/ProdutoForm.vue";

export default {
  name: "App",
  components: {
    NavbarComponents,
    ProdutoFormComponent,
  },
};
</script>

<style>
</style>
