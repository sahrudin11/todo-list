<script>
export default {
    data() {
        return {
            todo: '',
            savedTodo: []
        }
    },
    methods: {
        saveTodo(){
            this.savedTodo.push(this.todo)
            this.todo = ''
        },
        deleteTodo(index){
            this.savedTodo.splice(index, 1)
        }
    }
}
</script>

<template>
    <section>
        <section>
            <h1>Todo List App</h1>
            <p>Create Your Task Below</p>
            <div>
                <input v-model="todo" type="text">
                <button @click="saveTodo">Save</button>
            </div>
        </section>
        <section>
            <div class="todo-items" v-for="(todo, index) in savedTodo" :key="todo">
                <div class="todo-list">{{ index+1 }}. {{ todo }}</div>
                <button class="btn-danger" @click="deleteTodo(index)">Delete</button>
            </div>
        </section>
    </section>
</template>

<style scoped>
h1, p {
    text-align: center;
}

input, button{
    padding: 5px;
}
.todo-items{
    padding: 8px;
    border-radius: 8px;
    background-color: rgba(32, 32, 75, 0.877);
    margin: 15px 0;
    display: flex;
    justify-content: space-between;
}

.todo-list{
    padding: 6px;
}
.btn-danger{
    font-family: inherit;
    border: none;
    cursor: pointer;
    padding: 8px 12px;
    border-radius: 4px;
    background-color: rgba(52, 52, 88, 0.877);
    color: rgb(153, 24, 24);
}
</style>