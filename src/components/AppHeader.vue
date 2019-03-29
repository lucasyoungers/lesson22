<template>
  <header>
    <h2>My Awards</h2>
    <img id="logo" alt="Active Martial Arts Logo" src="../assets/active-logo.png">
  </header>
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
header {
  background-color: #666;
  padding: 10px;
  text-align: center;
  font-size: 4vw;
  color: white;
}

#logo {
  max-width: 100%;
}
</style>