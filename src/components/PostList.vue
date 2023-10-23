<template>
  <div>
    <h3>Список пользователей</h3>
    <post-item
      v-for="post in posts"
      v-bind:key="post.id"
      :post="post"
    />
  </div>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
  components: {
    PostItem
  },
  props: {
    posts: {
      type: Array,
      required: true
    }
  },
  data(){
    return {

    }
  }
}
</script>

<style scoped>

</style>
