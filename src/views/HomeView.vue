<script>
export default {
  data(){
    return{
      title: 'deploy-demo01',
      text: 'use sh deploy.sh'
    }
  }
}
</script>

<template>
  <div style="display: flex; flex-direction: column; justify-content: center;">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
  </div>
</template>
