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
            <p>Create your own todolist</p>
            <div>
                <input v-model="todo" type="text">
                <button @click="saveTodo">Save</button>
            </div>
        </section>
        <section>
            <div v-for="(todo, index) in savedTodo" :key="todo">
                <div>{{ todo }}</div>
                <button @click="deleteTodo(index)">Delete</button>
            </div>
        </section>
    </section>
</template>

<style scoped>
</style>