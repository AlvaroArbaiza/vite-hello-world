<script>
import AppTitle from './components/AppTitle.vue';

export default {
  name: "App",
  components: {
    AppTitle
  }
}
</script>

<template>
  <h1>La mia prima App con Vue!</h1>
  <AppTitle />
</template>

<style scoped>
h1 {
  color: green;
}
</style>
