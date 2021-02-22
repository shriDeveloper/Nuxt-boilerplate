<template>
  <div class="card mb-4">
    <div class="card-body">
      <nuxt-link :to="'/'+id" class="card-title">{{ title }}</nuxt-link>
    </div>
  </div>
</template>
<script>
export default {
  props: ["title","id"],
};
</script>

<style scoped>
.card:hover{
    cursor: pointer;
}
.card-title{
    text-decoration: none;
    color:black;
    text-transform: capitalize;
}
</style>