<template>
  <div id="app">
    <h1>Vue.js Vue TodoList</h1>
    <hr>
    <todoInput />
    <todoList />
    <p>todoList 数量：{{todoCount}}</p>
    <pre>{{$store.state}}</pre>
  </div>
</template>

<script>
  import todoInput from './components/input.vue';
  import todoList from './components/list.vue';
  import {mapGetters} from "vuex";

  export default {
    name: 'app',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    computed:{
      ...mapGetters({
        todoCount:"nCounts"
      })
    },
    components:{
      todoInput,
      todoList
    }
  }
</script>

<style lang="scss">
  %box{display:-webkit-box;-webkit-box-pack:center;-webkit-box-align:center;}
  #app{width:400px;margin:0 auto;}
  h1{text-align:center;}
</style>

