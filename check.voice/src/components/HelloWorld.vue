<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      全面提升学员听-说-读-写英语综合能力
    </h3>
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


<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
