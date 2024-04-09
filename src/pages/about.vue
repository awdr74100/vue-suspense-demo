<template>
  <h1>About</h1>
  <hr />
  <!-- <UserList /> -->
  <Suspense>
    <UserList #default />

    <template #fallback> Loading... </template>
  </Suspense>
</template>

<script setup lang="ts">
import UserList from '../components/UserList.vue';
</script>
