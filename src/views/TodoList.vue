<!-- TodoList.vue -->
<template>
    <div>
      <input v-model="novaTarefa" @keyup.enter="adicionarTarefa" placeholder="Adicionar tarefa" />
      <ul>
        <li v-for="(tarefa, index) in tarefas" :key="index">
          {{ tarefa }}
          <button @click="removerTarefa(index)">Remover</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        novaTarefa: '',
        tarefas: [],
      };
    },
    methods: {
      adicionarTarefa() {
        if (this.novaTarefa.trim() !== '') {
          this.tarefas.push(this.novaTarefa);
          this.novaTarefa = '';
        }
      },
      removerTarefa(index) {
        this.tarefas.splice(index, 1);
      },
    },
  };
  </script>
  