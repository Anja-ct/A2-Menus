<script setup>
import { ref, onMounted } from 'vue';

const msgVariable = ref('hello world');

const handleClick = (event) => {
  msgVariable.value = 'hejjj';
};

onMounted(() => {
  window.addEventListener('click', handleClick);
});
</script>

<template>
  <h1>{{ msgVariable }}</h1>
  <div class="square"></div>
</template>

<style scoped>
/* Styling af kvadrat */
.square {
  width: 300px;
  height: 100px;
  background-color: red;
  margin-top: 20px;
}
</style>
