<script setup lang="ts">
// See vite.config.ts for details about automatic imports
const route = useRoute();

useHead({
  title: () => route.meta.title || "Vite + Vue Template",
  meta: [
    {
      property: "og:title",
      content: () => route.meta.title,
    },
    {
      name: "twitter:title",
      content: () => route.meta.title,
    },
  ],
});
</script>
<template>
  <header class="h-14 bg-neutral-400 w-full"></header>
  <main class="">
    <router-view />
  </main>

  <footer class="h-14 bg-neutral-200"></footer>
</template>
