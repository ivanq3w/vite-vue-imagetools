<script setup lang="ts">
import { computed } from 'vue'
import iPumpkin from './assets/pumpkin.jpg?w=100&quality=30'

const iPumpkinUrl = computed(() => {
  return `url(${new URL(iPumpkin, import.meta.url).href})`
})
</script>

<template>
  <img class="cell" :src="iPumpkin" alt="" />
  <div class="cell pumpkin" style="height: 270px;"></div>
  <img class="cell" src="./assets/pumpkin.jpg?w=100&quality=1" alt="" >
</template>

<style>
.pumpkin {
  background: v-bind(iPumpkinUrl);
  background-size: 100%;
  background-repeat: no-repeat;
}
.cell {
  width: 400px;
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
  display: flex;
  flex-direction: column;
}
</style>
