<script>
import TheWelcome from '../components/TheWelcome.vue'
export default {
  data(){
    return{
      text: 'hi~~~'
    }
  }
}
</script>

<template>
  <h3>{{ text }}</h3>
  <main>
    <TheWelcome />
  </main>
</template>
