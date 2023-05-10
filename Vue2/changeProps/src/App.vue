<template>
  <div id="app">
    <inner :items="items"></inner>
    <br/>
    <div>
      Data{{ items }}
    </div>
  </div>
</template>

<script>
import inner from '@/components/inner'

export default {
  name: 'main-app',
  components: { inner },
  data() {
    return {
      items: [
        {
          id: 1,
          name: 'Dima'
        },
        {
          id: 2,
          name: 'Misha'
        },
      ]
    }
  }
}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
