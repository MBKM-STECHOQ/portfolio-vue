<template>
  <nav id="nav">
    <router-link to="/">Home</router-link> |
    <!-- <router-link to="/about">About</router-link> | -->
    <!-- to connect and redirect to designed route / Programmatic Route -->
    <router-link :to="{ name: 'Contact' }">Contact</router-link>
  </nav>
</template>

<script>
export default {
  name: 'the-nav',
};
</script>

<style lang="scss" scoped>
#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
