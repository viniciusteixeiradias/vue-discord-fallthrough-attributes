<script setup lang="ts">
defineProps<{
  button?: boolean;
  arrow?: boolean;
  nav?: boolean;
}>();
</script>

<template>
  <a
    :class="[
      'hover:underline cursor-pointer',
      button && 'hover-overlay rounded px-4 py-2 font-bold bg-teal-600',
      !nav && !button && 'text-teal-500',
      $attrs.class,
    ]"
  >
    <slot></slot>
  </a>
</template>
