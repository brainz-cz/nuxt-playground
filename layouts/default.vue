<template>
  <div>
    <nuxt/>
    <router-link :to="{ name: 'index'}">index</router-link>
    <router-link :to="{ name: 'about'}">about</router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      iterations: 5
    }
  }
}
</script>


<style lang="scss">
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}


ul{
  display: inline-block;
  padding: 0 !important;
  list-style: none;
  margin: 0;
}

.page-enter-active, .page-leave-active {

  h1{
    opacity: 1;
    transition: all 1s;
  }

  ul{
    li{
      transition: all .25s ease-out;
      transform: translate3d(0%, 0, 0);
      opacity: 1;
    }
  }
}
.page-enter, .page-leave-to {

  h1{
    opacity: 0;
  }

  ul{
    li{
      transform: translate3d(-100%, 0, 0);
      opacity: 0;
    }
  }
}
</style>
