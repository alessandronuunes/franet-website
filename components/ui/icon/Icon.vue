<script setup lang="ts">
import { computed } from 'vue';
import * as icons from 'lucide-vue-next';

interface Props {
  name: string;
  size?: number;
  color?: string;
  strokeWidth?: number;
  defaultClass?: string;
}

const props = defineProps<Props>();

const icon = computed(() => icons[props.name as unknown as keyof typeof icons]);
</script>

<template>
  <component
    :is="icon"
  />
</template>
