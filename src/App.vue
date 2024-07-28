<script setup>
import RecipeCard from '@/components/RecipeCard.vue';
</script>

<template>
  <main>
    <RecipeCard />
  </main>
</template>

<style scoped lang="scss">
@import '@/styles/base/media-queries';

main {
  @media #{$tablet-and-up} {
    padding: var(--spacing-1600) var(--spacing-600);
  }
}
</style>
