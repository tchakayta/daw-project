<!-- HelloWorld.vue -->
<template>
  <div>
    <p>Hello, World!</p>
  </div>
</template>

<!-- UserInfo.vue -->
<template>
  <div>
    <p>Nome: {{ nome }}</p>
    <p>Idade: {{ idade }}</p>
    <HelloWorld /> <!-- Usando o primeiro componente -->
  </div>
</template>

<script>
import HelloWorld from './HelloWorld.vue';

export default {
  components: {
    HelloWorld,
  },
  data() {
    return {
      nome: 'Seu Nome',
      idade: 25,
    };
  },
};
</script>
