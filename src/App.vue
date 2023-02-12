<script setup>
import { ref } from "vue";

const count = ref(0);

function increment() {
  count.value++;
}
function decrement() {
  count.value--;
}
function reset() {
  count.value = 0;
}
</script>

<template>
  <main>
    <div>
      <span>Count is: </span>
      <span
        ><em>
          {{ count }}
        </em>
      </span>
    </div>
    <button @click="decrement">-</button>
    <button @click="reset">reset</button>
    <button @click="increment">+</button>
  </main>
</template>

<style scoped>
main {
  font-size: 5rem;
}
button {
  font-size: inherit;
}
</style>
