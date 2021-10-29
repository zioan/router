<template>
  <h1>Job Detail Page</h1>
  <!-- <p>Job id is {{$route.params.id}}</p> -->
  <!-- <p>The job id is {{id}}</p> -->
  <p>The job id is {{myid}}</p>
</template>


<script>
  export default {
    props: ['myid'],
    // data() {
    //   return {
    //     id: this.$route.params.myid,
    //   }
    // }
  }
</script>

<style>

</style>