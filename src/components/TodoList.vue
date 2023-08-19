<script setup>
import { useTodoListStore } from "../stores/todoList.js";

const store = useTodoListStore();
</script>

<template>
  <ul>
    <li v-for="todo in store.todoList">
      {{ todo.item
      }}<button @click="store.deleteTodo(todo.id)">Delete Item</button>
    </li>
  </ul>
</template>

<style lang="scss" scoped></style>
