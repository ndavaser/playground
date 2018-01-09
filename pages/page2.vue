<template>
  <section class="container">
    <div>
      <h1 class="title">
        PAGE 2
      </h1>
      <h2 class="subtitle">
        My great 2nd page
      </h2>
      <p :key="key" v-for="(value, key) in exampleArray">{{ value }}</p>
      <strong>{{ title }}</strong>
      <strong>{{ body }}</strong>
      <div class="links">
        <a v-on:click="loadNext()" class="button--green button--green--great">Load different Async</a>
      </div>
    </div>
  </section>
</template>

<script>

import axios from 'axios'

export default {
  data () {
    return {
      id: 1,
      exampleArray: ['Lemon', 'Banana', 'Tree']
    }
  },
  methods: {
    async loadNext (event) {
      this.id = this.id + 1
      var { data } = await axios.get('https://jsonplaceholder.typicode.com/posts/' + this.id)
      this.title = data.title
      this.body = data.body
    }
  },
  async asyncData () {
    let { data } = await axios.get('https://jsonplaceholder.typicode.com/posts/1')
    return { title: data.title,
      body: data.body
    }
  }
}
</script>

<style>
.button--green--great
{
    cursor: pointer;
    margin-top: 30px;
}
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
</style>
