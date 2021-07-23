<template>
  <h1>{{ sus }}</h1>
  <button @click="randomSus">SUS</button>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import {susses} from "../assets/susses.js"

const sample = (arr: string[]) => {
  return arr[Math.floor(Math.random() * arr.length)];
};

const capitalize = (s: string) => {
  return s.charAt(0).toUpperCase() + s.slice(1);
}

export default defineComponent({
  name: 'SusGenerator',
  setup: () => {
    const sus = ref("sus");
    const randomSus = () => {
      sus.value = capitalize(sample(susses))
    }
    return { sus, randomSus}
  }
})
</script>

<style scoped>
button {
  padding: 10px 14px 10px 14px;
  align-items: baseline;
  color: white;
  background-color: #7b0838;
  border-radius: 10%;
  border-color: white;
}
</style>
