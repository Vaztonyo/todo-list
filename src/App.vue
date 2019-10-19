<template>
  <div id="app">
    <img id="img1" alt="Todo logo" src="./assets/List-PNG-Transparent-Picture.png">
    <TodoList v-bind:todos="todos"/>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'app',
  components: {
    TodoList
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo One",
          completed: false
        },
        {
          id: 2,
          title: "Todo Two",
          completed: false
        },
        {
          id: 3,
          title: "Todo Three",
          completed: false
        }
      ]
    }
  }
}
</script>

<style>
    * {
      box-sizing: border-box;
      margin: 5;
      padding: 5;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      line-height: 1.4;
    }
    #img1 {
      width: 20%;
      height: 20%;
    }
</style>
