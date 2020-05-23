<template>
  <div>
    <div>Count: {{ state.count }}</div>
    <button @click="increment">+</button>
  </div>
</template>

<script>
import { reactive } from 'vue'

export default {
  setup() {
    const state = reactive({
      count: 0
    });

    const increment = () => {
      state.count++;
    };

    return {
      state,
      increment
    };
  }
};
</script>
