<template>
  <div id="app" class="container">
      <div class="todo-wrapper">
          <todo-header></todo-header>
          <div class="todo-content">
          </div>
          <todo-report></todo-report>
          <todo-list>
          </todo-list>
      </div>
  </div>
</template>
<script>
import Header from './components/TodoHeader.vue';
import TodoReport from './components/TodoReport.vue';
import TodoList from './components/TodoList.vue';

export default {
    components: {
    "todo-header": Header,
    "todo-report": TodoReport,
    "todo-list": TodoList,
  }
}
</script>
<style lang = "stylus">
    
</style>


