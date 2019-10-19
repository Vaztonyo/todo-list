<template>
  <div>
    <h1>Todo List</h1>
    <div v-bind:key="todo.id" v-for="todo in todos">
    <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
    </div>
  </div>
</template>

<script type = "text/javascript" >
import TodoItem from './TodoItem.vue';

export default {
  name: "TodoList",
  components: {
    TodoItem
  },
  props: ["todos"]
};
</script>
<style scoped>
</style>
