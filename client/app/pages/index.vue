<template>
  <div class="container mx-auto p-4">
    Welcome, {{ user?.name }}!
  </div>
</template>

<script setup>
definePageMeta({
  middleware: 'sanctum:auth'
})

const { isAuthenticated, user } = useSanctumAuth()
</script>

<style scoped></style>