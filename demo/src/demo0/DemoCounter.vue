<script setup>
import { ref } from "vue";

const count = ref(0);

const increment = () => {
  count.value++;
};
const decrement = () => {
  count.value--;
};
</script>

<template>
  <div>
    <button @click="decrement">-</button>

    <span> Current value: {{ count }} </span>

    <button @click="increment">+</button>
  </div>
</template>

<style scoped lang="scss"></style>
