<template>
  <NuxtLink
    :class="{
      'border-primary hover:border-primary-light bg-primary-dark':
        variant === 'primary',
      'border-neutral-700 hover:border-neutral-600 bg-secondary-muted':
        variant === 'secondary',
      'bg-none': variant === 'ghost',
      'text-sm rounded-lg font-semibold hover:bg-neutral-800 px-4 py-2 flex justify-between gap-2 transition-colors': true,
    }"
  >
    <span v-if="prefixIcon" aria-hidden="true">
      {{ prefixIcon }}
    </span>

    <slot />

    <span v-if="suffixIcon" aria-hidden="true">
      {{ suffixIcon }}
    </span>
  </NuxtLink>
</template>

<script setup lang="ts">
type Props = {
  prefixIcon?: string
  suffixIcon?: string
  variant?: 'primary' | 'secondary' | 'ghost'
}

const { variant = 'primary' } = defineProps<Props>()
</script>
