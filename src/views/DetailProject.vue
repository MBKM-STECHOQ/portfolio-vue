<template>
  <div id="detail">
    <article v-if="projectById !== undefined">
      <h1>{{projectById.name}}</h1>
      <p>{{projectById.description}}</p>
      <img :src="projectById.image" :alt="projectById.description">
    </article>
    <article v-else>
      <h1>Project Not Found</h1>
    </article>
  </div>
</template>

<script>
export default {
  name: 'DetailProject',
  computed: {
    projectById() {
      return this.getProject.find((project) => project.id === this.$route.params.id);
    },
  },
};
</script>
