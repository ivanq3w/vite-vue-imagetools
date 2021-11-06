<script setup lang="ts">
import { computed } from 'vue'
import iPumpkin from './assets/pumpkin.jpg?w=100&quality=30'

const iPumpkinUrl = computed(() => {
  return `url(${new URL(iPumpkin, import.meta.url).href})`
})
</script>

<template>
  <img :src="iPumpkin" alt="" style="width: 400px;">
  <div class="pumpkin" style="width: 400px; height: 400px;"></div>
  <img src="./assets/pumpkin.jpg" alt="" style="width: 400px;">
</template>

<style>
.pumpkin {
  background: v-bind(iPumpkinUrl);
  background-size: 100%;
  background-repeat: no-repeat;
}
html, body {
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 0;
  margin: 0;
}
</style>
