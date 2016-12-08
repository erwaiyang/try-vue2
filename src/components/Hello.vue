<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ol>
      <li v-for="link in links">
        <a :href="link.url">{{ link.name }}</a>
      </li>
    </ol>
    <button v-on:click="toggleVisible">Toggle Visible</button>
    <h2 v-if="visible">{{ task }}</h2>
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
      links: [
        {
          name: 'blog',
          url: 'https://erwaiyang.github.io/blog',
        },
        {
          name: 'personal website',
          url: 'https://erwaiyang.github.io/',
        },
        {
          name: 'PaGamO',
          url: 'https://www.pagamo.org/',
        },
      ],
    };
  },
  methods: {
    toggleVisible() {
      this.visible = !this.visible;
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
