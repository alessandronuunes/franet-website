<script setup lang="ts">
import type { HTMLAttributes } from 'vue'
import { cn } from '~/lib/utils';

interface Props {
  class?: HTMLAttributes['class']
}

defineProps<Props>()
</script>

<template>
  <div :class="cn('flex items-center space-x-4', $props.class)">
    <slot />
  </div>
</template>
