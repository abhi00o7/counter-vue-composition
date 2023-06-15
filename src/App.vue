<script setup>
import { ref } from "vue";

const count = ref(0);

function increment() {
  count.value++;
}
function decrement() {
  console.log("loll........")

  count.value--;
}

function holdDecrement() {
  console.log("holdddddddddddddddd........")
  count.value--;
}

function reset() {
  count.value = 0;
}
</script>

<template>
  <main>
    <div class="ib">
      <span>Count is: </span>
      <span
        ><em>
          {{ count }}
        </em>
      </span>
    </div>
    <div class="ib">
      <button @click="decrement" @mousedown="holdDecrement" >-</button>
      <button @click="reset">reset</button>
      <button @click="increment">+</button>
    </div>
  </main>
</template>

<style scoped>
* {
  outline: 1px auto greenyellow;
}
main {
  height: 100vh;
  width: 100wh;
  display: flex;
  font-size: 5rem;
  align-items: center;
  justify-content: space-around;
}
.ib {
  display: inline-block;
  border: 1px solid #ccc;
}
div {
  position: sticky;
}
button {
  border-radius: 11%;
  font-size: 2rem;
}
</style>
