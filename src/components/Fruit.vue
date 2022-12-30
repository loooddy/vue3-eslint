<template>
  <li> {{ name }}?! </li>
</template>

<script>
  export default {
    props: {
      name: {
        type: String,
        default: ''
      }
    },
    data() {
      return{

      }
    }
  }
</script>

<style scoped lang="scss">
  h1{
    color: red !important;
  }
</style>