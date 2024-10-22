<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
       <router-link :to="{ name: 'JobDetails', params: {id: job.id}}">
            <h2>{{ job.title }}</h2>
       </router-link>
  </div>
</template>

<script>
export default {
    data(){
        return{
            jobs: [
                {title: 'Ninja UX Designer', id: 1, details: 'lorem'},
                {title: 'Ninja Web Developer', id: 2, details: 'lorem'},
                {title: 'Ninja Vue Developer', id: 3, details: 'lorem'}
            ]
        }
    }
}
</script>

<style>
    .job h2 {
        background: #f4f4f4;
        padding: 1.25rem;
        border-radius: .625rem;
        margin: .625rem auto;
        max-width: 37.5rem;
        cursor: pointer;
        color: #444;
    } 
    .job h2:hover {
        background: #ddd;
    }
    .job a {
        text-decoration: none;
    }
</style>