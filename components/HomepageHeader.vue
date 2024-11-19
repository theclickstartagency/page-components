<template>
  <div>
    <h1 :class="styles.title">{{ title }}</h1>
    <h2 :class="styles.subtitle">{{ subtitle }}</h2>
    <div :class="styles.content" v-html="content"></div>
  </div>
</template>

<script setup lang="ts">
  const props = defineProps({
    title: {
      type: String,
      default: 'Title'
    },
    subtitle: {
      type: String,
      default: 'Subtitle'
    },
    content: {
      type: String,
      default: 'Content'
    },
    styles: {
      type: Object,
      default: {
        title: 'text-red',
        subtitle: 'text-blue',
        content: 'text-green'
      }
    }
  })
</script>

<style scoped></style>
