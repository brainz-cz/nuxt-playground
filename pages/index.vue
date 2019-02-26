<template>
  <div>
    <h1 class="title">
      {{ title }}
    </h1>
    <ul>
      <li
        v-for="(i, key) in 10"
        :key="key"
        :style="{'transition-delay': i * 100 + 'ms'}"
      >
        Ipsum lorem dolor ipsum {{ i }}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  transition: {
    name: 'page',
    mode: 'out-in',
    duration: '1300'
  },
  components: {
  },
  data() {
    return {
      subtitle: 'some'
    }
  },
  mounted() {

  },
  async asyncData(context) {
    var { data } = await context.$axios.get('https://jsonplaceholder.typicode.com/todos/1')
    return {
      ...data
    }
  }
}
</script>

<style>

</style>
