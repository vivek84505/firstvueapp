<template>
    <h5>Todo List</h5>
    <todo v-for="(todo,index) in todos" :key="index" :todo="todo"></todo>
</template>



<script>
import { mapState } from "vuex"
import Todo from './Todo.vue'
export default {
    components:{
        Todo
    },
    computed:{
         ...mapState({
            todos:'todos'
         })
    }
}
</script>

<style>

</style>

