<template>
  <NavBar />
  <div class="container is-max-desktop px-2 py-4">
    <RouterView />
  </div>
</template>

<script setup>
import { onMounted } from 'vue';
import NavBar from '@/components/Layout/NavBar.vue';
import { useStoreNotes } from '@/store/storeNotes';

const storeNotes = useStoreNotes();

onMounted(() => {
  storeNotes.getNotes();
});
</script>

<style>
@import 'bulma/css/bulma.min.css';
</style>