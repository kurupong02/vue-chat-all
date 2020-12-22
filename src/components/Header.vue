<template>
  <div class="header">
    <div>Messages</div>
    <div>dsad</div>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  box-shadow: 0 0 1px rgba(0, 0, 0, 0.25);
  transition: background-color 0.3s ease-in-out;
  background-color: #fff;
  height: 40px;
  z-index: 20;
  align-items: center;
  padding: 0px 10px;
}
</style>
