<template>
  <h2>UserList</h2>
  <ul>
    <li v-for="(user, index) in users" :key="index">
      <p>Id: {{ user.id }}</p>
      <p>Name: {{ user.name }}</p>
      <p>Email: {{ user.email }}</p>
    </li>
  </ul>
</template>

<script setup lang="ts">
import type { User } from '../types';

const users = await fetch('https://jsonplaceholder.typicode.com/users', { method: 'get' }).then(
  (res) => res.json() as Promise<User[]>,
);
// import { ref } from 'vue';
// import type { User } from '../types';

// const users = ref<User[]>([]);

// async function getUserList() {
//   users.value = await fetch('https://jsonplaceholder.typicode.com/users', { method: 'get' }).then(
//     (res) => res.json() as Promise<User[]>,
//   );
// }

// getUserList();
</script>
