<template>
    <div>
        <form @submit="addTodo">
            <input v-model="title" type="text" name="title" placeholder="add todo..">
            <input type="submit" value="submit" class="btn">
        </form>
    </div>
</template>

<script>
    // import uuid from 'uuid';
    export default {
        name:"AddTodo",
        data(){
            return {
                title:''
            }
        },
        methods:{
            addTodo(e){
                e.preventDefault();
                const newTodo={
                    // id:uuid.sv4(),
                    title:this.title,
                    completed:false
                }

                // send up to parent
                this.$emit('add-todo',newTodo);

                // clear
                this.title='';
            }
        }
    }
</script>

<style scoped>
    form{
        display: flex;
    }

    input[type="text"]{
        flex:10;
        padding:5px;
    }

    input[type="submit"]{
        /* color:'yellow'; */
        flex:2;
    }
</style>
