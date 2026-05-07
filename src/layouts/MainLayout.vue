<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="layout-header">
    <div class="layout-nav">
      <RouterLink to="/" class="nav-link">Home</RouterLink>
      <RouterLink to="/about" class="nav-link">About</RouterLink>
    </div>
  </header>

  <main class="layout-main">
    <RouterView />
  </main>

  <footer class="layout-footer">
    <p>&copy;{{ new Date().getFullYear() }} interset-wq</p>
  </footer>
</template>

<style scoped>
.layout-header {
  border-bottom: 1px solid #e5e7eb;
  background-color: skyblue;
  height: 50px;
  width: 100vw;
  padding: 0 2rem;
}

.layout-nav {
  display: flex;
  gap: 2rem;
  height: 50px;
  /* 与 header 高度保持一致，才能垂直居中 */
  align-items: center;
}

.nav-link {
  text-decoration: none;
  font-size: 1.25rem;
  color: #42b883;
  font-weight: 600;
  transition: color 0.2s;
}

.nav-link:hover {
  color: #35495e;
}

.nav-link.router-link-exact-active {
  color: #35495e;
  border-bottom: 2px solid #35495e;
}

.layout-main {
  flex: 1;
  padding: 1rem 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.layout-footer {
  height: 50px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  border-top: 1px solid #e5e7eb;
  padding: 1rem 2rem;
  color: #6b7280;
  /* background-color: #f9fafb; */
  background-color: skyblue;
}

.layout-footer p {
  margin: 0;
}
</style>
