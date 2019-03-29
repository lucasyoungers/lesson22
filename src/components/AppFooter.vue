<template>
  <footer class="container">
    <p>copyright Active Martial Arts</p>
  </footer>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
footer {
  background-color: #777;
  padding: 10px;
  text-align: center;
  color: white;
}
</style>