<script setup lang="ts">
import { ref } from "vue";
const message = ref('dattx');
const seen = ref(true);
const count = ref(0);
const todos = ref([{
  id: 1,
  text: "Learn HTML",
  done: true
},
{ 
  id: 2,
  text: "Learn CSS",
  done: true
},
{
  id: 3,
  text: "Learn Vue",
  done: false
},
{
  id: 4,
  text: "Build something awesome",
  done: false
},
{
  id: 5,
  text: "Build something awesome 2",
  done: false
},
{
  id: 6,
  text: "Build something awesome 3",
  done: false
}
]);


const objAtrs = {
  id: "app-2",
  style: {
    color: "red",
    cursor: "pointer"
  }
}


</script>

<template>
  <div style="display: flex; flex-direction: column; justify-content: center; align-items: center;">
    <div id="header">todos</div>
  <div  id="container">
    <div v-for="todo in todos">
      <span :key="todo.id">{{ todo.text }}</span>
      <button @click="todos.pop()">delete</button>
    </div>
  </div>
  </div>
  
</template>

<style scoped>
#header{
  text-transform: uppercase;
  font-size: x-large;
}

#container{
  display: flex;
  flex-direction: column;
  background-color: antiquewhite;
}
</style>
