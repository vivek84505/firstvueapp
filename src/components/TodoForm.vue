<template>
    <div>
        <input type="text" v-model="newTodoItem">
        <button @click="addnewTodoItem">submit</button>
    </div>
</template>


<script>
export default {
     data(){
        return{
            newTodoItem:""
        }
     },
     methods:{
        addnewTodoItem(){
            this.$store.dispatch('addNewTodo',this.newTodoItem);
            this.newTodoItem="";
        }
     }
}
</script>