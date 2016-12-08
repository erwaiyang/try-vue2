<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 v-if="visible">{{ task }}</h2>
    <button v-on:click="writeConsole">Click Me then Open Your Console</button>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      msg: 'This Is My First Vue App',
      task: 'now what?',
      visible: true,
    };
  },
  methods: {
    writeConsole() {
      console.warn('hello!');
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
