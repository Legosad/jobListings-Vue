<script setup>
import jobData from "@/jobsData.json"
import { ref } from "vue";
const jobs = ref(jobData)
    console.log(jobs.value)
</script>
<template>
    <section class></section>
    <div v-for="job in jobs" :key="job.id">{{ job.title }}</div>
</template>