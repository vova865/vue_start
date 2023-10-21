<template>
  <form @submit.prevent>
    <h4>Создане поста</h4>
    <input v-bind:value="title" @input="inputTitle" class="input" type="text" placeholder="Название">
    <input v-bind:value="body" @input="inputBody" class="input" type="text" placeholder="Описание">
    <button class="btn" @click="createPost">Создать пост</button>
  </form>
</template>

<script>
export default {
  name: "PostForm"
}
</script>

<style scoped>

</style>
