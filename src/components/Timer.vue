<template>
  <button @click="increment">Кнопка нажата {{ clickCount }} раз</button>
</template>

<script setup>
import { ref, onMounted } from "vue";
const clickCount = ref(0);

function increment() {
  clickCount.value++;
}

onMounted(() => {
  console.log(`The initial count is ${clickCount.value}.`);
});

defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
