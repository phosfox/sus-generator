<template>
  <img alt="Amogus" src="./assets/amogus.png" :style="{width: '400px', height: auto}" />
  <SusGenerator/>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import SusGenerator from './components/SusGenerator.vue'

export default defineComponent({
  name: 'App',
  components: {
    SusGenerator
  }
})
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
