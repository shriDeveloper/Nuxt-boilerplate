<template>
  <div class="container mt-4">
    <nav aria-label="breadcrumb">
      <ol class="breadcrumb">
        <li class="breadcrumb-item"><nuxt-link to="/">Back</nuxt-link></li>
        <li class="breadcrumb-item active" aria-current="page">Current</li>
      </ol>
    </nav>
    <h1>Showing Results for : {{ id }}</h1>
  </div>
</template>

<script>
import Todo from "../../components/Todo";
export default {
  components: {
    Todo,
  },
  data() {
    return {
      id: this.$route.params.id,
    };
  },
};
</script>

<style>
.breadcrumb{
    background-color:whitesmoke;
}
</style>
