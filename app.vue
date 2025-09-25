<template>
  <div>
    <nav>
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
      <NuxtLink to="/posts">Posts</NuxtLink>
    </nav>
    <hr>
    <NuxtPage /> <!-- This is where your page content will be rendered -->
  </div>
</template>

<style scoped>
nav {
  padding: 1rem;
  background-color: #f0f0f0;
}
nav a {
  margin-right: 1em;
  text-decoration: none;
  color: #333;
}
nav a:hover {
  color: #007bff;
}

hr {
  margin: 1rem 0;
  border: 0;
  height: 1px;
  background: #eee;
}
</style>
