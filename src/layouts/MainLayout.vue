<template>
  <div class="main">
    <sidebar />
    <div class="container">
      <header-component></header-component>
      <slot></slot>
    </div>
  </div>
</template>

<script>
import Sidebar from "../components/Sidebar.vue";
import HeaderComponent from "../components/Header.vue";

export default {
  name: "MainLayout",
  components: {
    Sidebar,
    HeaderComponent
  }
};
</script>

<style>
.main {
  display: flex;
}
.container {
  flex: 1;
}
</style>
