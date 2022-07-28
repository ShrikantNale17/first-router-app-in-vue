<template>
  <div>
    <h1>Jobs Page</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
        <h2>{{ job.title }}</h2>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { id: 1, title: "UI/UX", desc: "lorem" },
        { id: 2, title: "React Developer", desc: "lorem" },
        { id: 3, title: "Angular Developer", desc: "lorem" },
        { id: 4, title: "Vue Developer", desc: "lorem" },
      ],
    };
  },
};
</script>

<style scoped>
.job h2 {
  background-color: rgb(227, 231, 231);
  padding: 20px;
  margin: 10px auto;
  border-radius: 10px;
  max-width: 600px;
  cursor: pointer;
  color: rgb(70, 70, 70);
}

.job h2:hover {
  background: rgb(202, 202, 202);
}

.job a {
  text-decoration: none;
}
</style>
