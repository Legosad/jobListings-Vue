<script>
export default {
  data() {
    return {
      name: "John Doe",
      status: '',
      tasks: ['Task one', 'Task two', 'Task three'],
      link: "https://www.google.com"
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === "active") {
        this.status = 'pending';
      } else if (this.status === "pending") {
        this.status= 'inactive'
      } else {
        this.status = 'active'
      }
      }
    }
  }
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status==='active'">User is Active</p>
  <p v-else-if="status==='pending'">User is Pending</p>
  <p v-else>User is Inacive</p>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <!-- <a v-bind:href="link" target="_blank">Click for google</a> -->
  <a :href="link" target="_blank">Click for google</a>
  <br/>
  <button @click="toggleStatus">Change status</button>

</template>