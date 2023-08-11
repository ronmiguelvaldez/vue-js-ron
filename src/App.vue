<template>
  <div id="app">
    <p> Number: {{ number }} <!-- ${number}--> </p>
    <button @click="decrease">decrease</button>
    <button @dblclick="reset">reset</button>
    <button @click="increase">increase</button><br>
    <label> Note: Double Click for Reset</label> <br>
    <br>
    <label> Input your name</label>
    <input type="text" @keydown.enter="showinput" v-model="name"> <br>
    <button @click="removetext"> Remove Text </button>
    <p>Hello, {{ showName }}</p>
  </div>
</template>

<script>
  export default {
    components: {
      
    },
    data() {
      return {
         number: 0,
         name: '',
         showName: ''
      }
    },
    methods: {
      decrease() {
        return this.number -= 1
      },
      reset() {
        this.number = 0
      },
      increase() {
        return this.number += 1
      },
      showinput() {
        this.showName = this.name
      },
      removetext() {
        this.showName = '';
        this.name = ''
      }
    }
  }
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
/*button {
  background: black;
  color: white;
}
button:hover {
  background: grey;
  color: black;

}*/
</style>
