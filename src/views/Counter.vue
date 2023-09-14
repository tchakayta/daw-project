<!-- Counter.vue -->
<template>
  <div>
    <p>Número: {{ numero }}</p>
    <button @click="increment">Incrementar</button>
    <button @click="decrement">Decrementar</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numero: 0,
    };
  },
  methods: {
    increment() {
      this.numero++;
    },
    decrement() {
      this.numero--;
    },
  },
};
</script>
