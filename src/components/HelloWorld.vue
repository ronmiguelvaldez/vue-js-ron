<template>
  <div class="hello">
    <h1>
      {{ number }}
    </h1>
    <button @click="decrease">decrease</button>
    <button @click="reset">reset</button>
    <button @click="increase">increase</button><br />
    <label> Note: Double Click for Reset</label> <br />
    <br />
    <label> Input your name</label>
    <input type="text" @keydown.enter="showinput" v-model="name"/> <br>
    <button @click="removetext">Remove Text</button>
    <p>Hello, {{ showName }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  data() {
    return {
      number: 0,
      name: "",
      showName: "",
    };
  },
  methods: {
    decrease() {
      return (this.number -= 1);
    },
    reset() {
      this.number = 0;
    },
    increase() {
      return (this.number += 1);
    },
    showinput() {
      this.showName = this.name;
    },
    removetext() {
      this.showName = "";
      this.name = "";
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
