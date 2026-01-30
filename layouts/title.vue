<script setup lang="ts">
withDefaults(defineProps<{
  topImage?: string
  bottomImage?: string
}>(), {
  topImage: '/Python-Red.webp',
  bottomImage: '/Tokyo-Background.webp',
})
</script>

<template>
  <div
    class="slidev-layout title-slide flex flex-col h-full bg-white relative overflow-hidden"
  >
    <!-- Top Image Section -->
    <div class="flex justify-center pt-12">
      <img
        v-if="topImage"
        :src="topImage"
        class="h-18 object-contain"
        alt="Top Image"
      />
    </div>

    <!-- Content Section (Title & Subtitle) -->
    <div
      class="flex-grow flex flex-col items-center justify-center text-center z-10 px-8"
    >
      <slot />
    </div>

    <!-- Bottom Image Section -->
    <div class="w-full mt-auto">
      <img
        v-if="bottomImage"
        :src="bottomImage"
        class="w-full object-contain object-bottom"
        alt="Bottom Image"
      />
    </div>
  </div>
</template>

<style scoped>
.title-slide {
  color: inherit;
}

/* Scoped styles for title and subtitle */
:deep(h1) {
  @apply text-5xl font-bold mb-4 leading-tight;
  color: black;
}

:deep(h2),
:deep(p) {
  @apply text-2xl font-medium opacity-90;
}

:deep(h2) {
  color: var(--tokyo-gray);
}

:deep(p) {
  @apply black;
}
</style>
