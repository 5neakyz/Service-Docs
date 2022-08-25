<script setup>
import TheWelcome from "@/components/TheWelcome.vue";
import SideNav from "@/components/SideNav.vue";
</script>

<template>
  <nav class="sidenav">
    <SideNav />
  </nav>
  <main class="main">
    <TheWelcome />
  </main>
</template>
<style scoped>
@media (min-width: 1024px) {
  .main {
    max-width: 1080px;
    margin: 0 auto;
    padding: 0rem;
    font-size: 1.4rem;
    font-weight: normal;
  }
  .sidenav {
    position: fixed;
    float: left;
    font-size: 1.4rem;
    font-weight: normal;
  }
}
</style>
