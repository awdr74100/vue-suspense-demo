<template>
  <ul>
    <li v-for="(route, index) in routes" :key="index">
      <RouterLink :to="{ path: route.path }">{{ route.path }}</RouterLink>
    </li>
  </ul>
  <RouterView />
</template>

<script setup lang="ts">
import { routes } from 'vue-router/auto-routes';

console.log(routes);

</script>
