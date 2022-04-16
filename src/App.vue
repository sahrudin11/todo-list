<script>
  import TodoList from './components/TodoList.vue'
  export default {
    components: {
      TodoList
    }
  }
</script>

<template>
  <main>
    <TodoList></TodoList>
  </main>
</template>

<style>
  body{
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: rgb(17, 66, 20);
    color: white;
    box-sizing: border-box;
  }
  main{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
