<script setup>
import HelloWorld from './components/HelloWorld.vue'
import { DxDateBox } from '../bundles/devextreme-vue-bundle.mjs'
import { ref } from 'vue'

const startValue =ref(new Date())
const endValue = ref(new Date())
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />

  <DxDateBox
      v-model:value="startValue"
      v-model:max="endValue"
  />
  <DxDateBox
      v-model:value="endValue"
      v-model:min="startValue"
  />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
