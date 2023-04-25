<template>
  <div class="hello">
    {{ greetings }}
  </div>
</template>

<script>
import { eventBus } from '@/main'

export default {
  name: 'HelloWorld',
  data() {
    return {
      greetings: ''
    }
  },
  created() {
    eventBus.$on('sayHi', data => {
      this.greetings = data.data
    })
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
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
