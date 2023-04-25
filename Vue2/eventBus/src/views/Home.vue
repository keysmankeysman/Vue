<template>
  <div class="home">
    <button @click="sendEvent">Передать event в компонент HelloWorld</button>
  </div>
 </template>
 
<script>
import { eventBus } from '@/main'

 export default {
   name: 'home',
    components: {},
    data() {
      return {
        greetings: 'Привет'
      }
    },
    methods: {
      sendEvent() {
        eventBus.$emit('sayHi', {
          data: this.greetings,
        })
      }
    }
    
 }
</script>
 
<style>

.form-control {
  padding: 5px;
} 

.form-control label {
  display: block;
}
    
.send {
  margin: 5px;
}
    
</style>