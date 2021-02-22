<template>
  <div class="container mt-4">
    <Todo v-for="(todo,index) in todos" :id="index" :key="index" :title="todo.title"></Todo>
  </div>
</template>

<script>
import Todo from '../components/Todo';


const axois = require('axios');

export default {
  components:{
    Todo,
  },
   data(){
        return {
            todos:[],
        }
    },
    async created(){
        try {
            const response = await axois.get('https://jsonplaceholder.typicode.com/todos');    
            this.todos = response.data;
            console.log(this.todos);
        } catch (error) {
            console.log(err);
        }
    },
     mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  }
}
</script>

<style>
</style>
