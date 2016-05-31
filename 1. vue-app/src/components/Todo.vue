<template>
  <article>
    <h1>Vue to-do list!</h1>
    <hr/>

    <ul>
      <li v-if="!todoList.length"><h3>No items in the list 🤔</h3></li>
      <li v-for="todo in todoList">
        <p @click="toggleDone(todo)" :class="{done: todo.done}">
          <span v-if="!todo.done">🔲</span>
          <span v-if="todo.done">✅</span>
          <b>{{todo.name}}</b>
        </p>
      </li>
    </ul>

    <form @submit.prevent="addTodo">
      <input type="text" v-model="currentTodo" placeholder="Type a new todo item" />
      <button type="submit">📝 Add!</button>
    </form>

    <hr/>
    <button v-if="todoList.length && doneItemsExist()" @click.prevent="clearDone">😵 Clear done!</button>
  </article>
</template>

<script>
export default {
  data () {
    return {
      todoList: [],
      currentTodo: ''
    }
  },

  methods: {
    addTodo: function addTodo () {
      this.todoList.push({name: this.currentTodo, done: false})
      this.currentTodo = ''
    },

    toggleDone: function toggleDone (todo) {
      todo.done = !todo.done
    },

    clearDone: function clearDone () {
      this.todoList = this.todoList.filter(function filterTodo (todo) {
        return !todo.done
      })
    },

    doneItemsExist: function doneItemsExist () {
      return this.todoList.reduce(function checkIfItemsDone (prev, cur) {
        return cur.done || prev
      }, false)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}

input{
  padding:10px 15px;
  font-size:1.1em;
  min-height:27px;
}

button{
  border-radius:0;
  background-color: gray;
  border:1px solid grey;
  padding:10px 30px;
  color:white;
  font-size:1.1em;
  font-weight:300;
}

button[type="submit"]{
  background-color: #42b983;
  border:1px solid #42b993;
}

p{
  display:flex;
  justify-content: center;
  align-items: center;
  line-height:1.3em;
}

p.done{
  opacity: 0.6;
}

p.done b{
  text-decoration: line-through;
}

ul{
  list-style-type: none;
  margin:30px 0;
  padding: 0;
}

ul li p{
  cursor:pointer;
}

li{
  margin:0 15px;
  padding:0 15px;
}

li * {
  font-weight:300;
}

li span{
  margin-right:5px;
  font-size:1.2em;
}

hr{
  margin:30px 0;
  border: 1px solid whitesmoke;
}
</style>
