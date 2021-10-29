<template>
  <div v-if="job">
    <h1>{{job.title}}</h1>
    <p>The job id is {{myid}}</p>
    <p>{{job.details}}</p>
  </div>
  <div v-else>
    <p>Loading job details...</p>
  </div>
</template>


<script>
  export default {
    props: ['myid'],
    data(){
      return {
        job: null
      }
    },
    mounted() {
      fetch("http://localhost:3000/jobs/" + this.myid)
      .then((res) => res.json())
      .then((data) => this.job = data)
      .catch((err) => console.log(err))
    }
  }
</script>

<style>

</style>