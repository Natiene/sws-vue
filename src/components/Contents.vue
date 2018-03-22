<template>
  <div>
    {{mostrar}}


  </div>

</template>

<script>
  import axios from 'axios'
  export default {
    name: "contents",
    data() {
      return {
        'mostrar': [],
      }

    },
    created() {
      axios.get("https://swapi.co/api/people/1").then(response => {
        this.mostrar = response.data
        console.log(response)

      })
    }
  }




</script>

<style scoped>

</style>
