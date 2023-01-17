<template>
  <div id="app">
  <h1>vue learning goals</h1>
   <input type="text" v-model="enteredValue"></input>
   <button @click="addGoal()"> add goals
      </button>
   <ul>
   <li v-for = "goal in goals">{{goal}}
   </li > 
   </ul>
   <p>learn <a v-bind:href="vuelink"> vue</a></p>
  </div>
</template>

<script>

export default {
  data() {
      return {
        goals: [],
        enteredValue: '',
        vuelink :'https://vuejs.org/tutorial/#step-1'
      }},

  methods : 
  {
    addGoal(){
      this.goals.push(this.enteredValue)
      this.enteredValue=""
    }

  }
  }

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
