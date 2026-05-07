<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="layout">
    <header class="layout-header">
      <div class="layout-nav">
        <RouterLink to="/" class="nav-link">Home</RouterLink>
        <RouterLink to="/" class="nav-link">About</RouterLink>
      </div>
    </header>

    <main class="layout-main">
      <RouterView />
    </main>

    <footer class="layout-footer">
      <p>&copy;2026 interset-wq</p>
    </footer>
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  margin: 0;
}

.layout-header {
  border-bottom: 1px solid #e5e7eb;
  background-color: skyblue;
  height: 50px;
  padding: 0 2rem;
}

.layout-nav {
  display: flex;
  gap: 2rem;
  height: 50px; /* 与 header 高度保持一致，才能垂直居中 */
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
  justify-content: center; /* 新增：内容垂直居中 */
}

.layout-footer {
  border-top: 1px solid #e5e7eb;
  text-align: center;
  padding: 1.5rem 0;
  font-size: 0.9rem;
  color: #6b7280;
  background-color: #f9fafb;
}
</style>
