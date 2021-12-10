<template>
  <h1>Vue 3 Todo App</h1>
  <form action="" @submit.prevent="addNewTodo">
    <label for="New Todo"></label>
    <input v-model="newTodo" name="newTodo" type="text" />
    <button>Add New Todo</button>
  </form>
  <h2>{{ newTodo }}</h2>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const newTodo = ref("");
    function addNewTodo() {
      console.log("submitted bro");
      console.log(newTodo.value);
    }
    return {
      addNewTodo,
      newTodo,
    };
  },
};
</script>

<style></style>
