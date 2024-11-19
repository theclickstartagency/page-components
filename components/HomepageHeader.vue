<template>
  <div>
    <h1 :class="classes.title">{{ title }}</h1>
    <h2 :class="classes.subtitle">{{ subtitle }}</h2>
    <div :class="classes.content" v-html="content"></div>
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
    classes: {
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
