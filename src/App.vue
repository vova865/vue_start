<template>
  <div class="app">
  </div>
</template>

ОСТАНОВИЛСЯ НА 33:25

<script>
export default {
  data(){
    return {
      posts: [
        {id: 1, title: 'Javascript', body: 'Описание поста   '},
        {id: 2, title: 'Javascript 2', body: 'Описание поста 2 '},
        {id: 3, title: 'Javascript 3', body: 'Описание поста 3 '},
      ],
      title: '',
      body: '',
    }
  },
  methods: {
    createPost() {
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body
      }
      this.posts.push(newPost);
      this.title = '';
      this.body = '';
    },
    inputTitle(event) {
      this.title = event.target.value;
    },
    inputBody(event) {
      this.body = event.target.value;
    },
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}

.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 15px;
}

form {
  display: flex;
  flex-direction: column;
}

.btn {
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background :none;
  color: teal;
  border: 1px solid teal;
}
</style>
