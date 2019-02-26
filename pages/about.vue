<template lang="html">
  <div>
    <h1 class="title">
      About page
    </h1>

    <ul>
      <li
        v-for="(i, key) in 10"
        :key="key"
        :style="{transitionDelay: i * 100 + 'ms'}"
      >
        Lorem ipsum {{ i }}, {{ key }}
      </li>
    </ul>

    <p>Lorem ipsum dolor sit amet</p>
  </div>
</template>

<script>
export default {
  transition: {
    name: 'page',
    mode: 'out-in',
    duration: '1300'
  }
}
</script>

<style lang="css">

</style>
