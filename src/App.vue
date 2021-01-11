<template>
  <div id="app">
    <HaxButton
      size="big"
    >123</HaxButton>
  </div>
</template>

<script>
import HaxButton from '@/components/HaxButton.vue';
export default {
  name: 'App',
  components: {
    HaxButton
  }
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
