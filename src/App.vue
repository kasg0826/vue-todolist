<template>
  <div id="app">
    <todo-list v-bind:todos="todos"></todo-list>
    <create-todo v-on:create-todo="addTodo"></create-todo>
  </div>
</template>

<script>
import TodoList from './components/TodoList'
import CreateTodo from './components/CreateTodo'

export default {
  name: 'app',
  components: {
    TodoList,
    CreateTodo
  },

  data () {
    return {
      todos: [{
        title: 'Todo A',
        project: 'Project A',
        finished: false
      },
      {
        title: 'Todo B',
        project: 'Project B',
        finished: false
      },
      {
        title: 'Todo C',
        project: 'Project C',
        finished: false
      },
      {
        title: 'Todo D',
        project: 'Project D',
        finished: false
      }]
    }
  },

  methods: {
    addTodo (newTodo) {
      this.todos.push(newTodo)
    }
  }
}
</script>
