<template>
  <div class="pupil">
    <h1>以下是我们的学员</h1>
    <ul v-for="post in posts" v-bind:key="post.id">
      <li>{{ post.name }}</li>
      <li>{{ post.comment }}</li>
    </ul>
  </div>
</template>

<script lang="ts">
  export default {
    data() {
      return {
        posts: [],
      };
    },

    methods: {
      async getData() {
        try {
          let response = await fetch("https://raw.githubusercontent.com/weijiang2023/check.voice/main/data/pupil.json");
          this.posts = await response.json();;
        } catch (error) {
          console.log(error);
        }
      },
    },

    created() {
      this.getData();
    },
  };
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
