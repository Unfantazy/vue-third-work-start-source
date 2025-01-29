<script setup>
import { ref } from "vue";
import CounterButton from "./CounterButton.vue";
import CounterValue from "./CounterValue.vue";

const count = ref(0);

const increment = () => {
  count.value++;
};
const decrement = () => {
  count.value--;
};
</script>

<template>
  <div class="counter">
    <counter-button @action="decrement">-</counter-button>
    <counter-value :value="count" />
    <counter-button @action="increment">+</counter-button>
  </div>
</template>

<style lang="scss" scoped>
.counter {
  display: flex;
  align-items: center;

  button {
    margin: 0 10px;
    font-size: 1.5rem;
    width: 2rem;
    height: 2rem;
    border-radius: 50%;
    border: none;
    background: #dd0000;
    color: white;
    cursor: pointer;

    &:hover {
      background: #ff0000;
    }
  }
}
</style>
