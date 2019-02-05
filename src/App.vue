<template>
  <div id='app'>
    <img alt='Vue logo' src='./assets/logo.png'>
    <Table :markSheet="markSheet" />
  </div>
</template>

<script>
import Table from './components/Table'

export default {
  name: 'app',
  components: {
    Table
  },
  data () {
    return {
      markSheet: [
        {
          subject: 'math',
          marks: 80
        },
        {
          subject: 'science',
          marks: 70
        },
        {
          subject: 'తెలుగు',
          marks: 90
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
