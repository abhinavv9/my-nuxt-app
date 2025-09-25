<template>
  <div>
    <h1>Blog Posts</h1>
    <div v-if="pending">Loading posts...</div>
    <div v-else-if="error" class="error">
      <p>Error loading posts: {{ error.message }}</p>
    </div>
    <ul v-else>
      <li v-for="post in posts" :key="post.id" class="post-item">
        <h2>{{ post.title }}</h2>
        <p>{{ post.body }}</p>
      </li>
    </ul>
  </div>
</template>

<script setup>
// Use useFetch to fetch data from an API
const { data: posts, pending, error } = await useFetch('https://jsonplaceholder.typicode.com/posts?_limit=10');
</script>

<style scoped>
div {
  padding: 2rem;
}
.error p {
  color: red;
  font-weight: bold;
}
.post-item {
  margin-bottom: 1.5rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid #eee;
}
.post-item h2 {
  margin-bottom: 0.5rem;
  color: #333;
}
.post-item p {
  color: #666;
}
</style>
