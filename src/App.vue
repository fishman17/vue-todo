<template>
  <div id="app" class="container">
      <div class="todo-wrapper">
          <todo-header></todo-header>
          <div class="todo-content">
          </div>
          <todo-report></todo-report>
          <todo-list  :collection="listState.items"> </todo-list>
      </div>
  </div>
</template>
<script>
import Header from './components/TodoHeader.vue';
import TodoReport from './components/TodoReport.vue';
import TodoList from './components/TodoList.vue';
import ListStore from '../data/store.js';
export default {
    data(){
        return{
            listState: ListStore.state
        }
    },
    components: {
    "todo-header": Header,
    "todo-report": TodoReport,
    "todo-list": TodoList,
  }
}
</script>
<style lang = "stylus">
    @import "../styl/style.styl";
</style>


