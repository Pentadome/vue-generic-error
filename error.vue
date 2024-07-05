<script setup lang="ts" generic="T extends 'checkbox' | 'radio'">
defineProps<{
  type: T;
}>();

defineModel<boolean>({ required: true });
</script>

<template>
  <div class="relative size-5">
    <input
      v-model="modelValue"
      :type="type"
      class="peer absolute left-0 top-0 size-full appearance-none" />
    <div
      aria-hidden="true"
      class="pointer-events-none absolute size-full border border-primary2 p-1 peer-checked:*:block peer-[&[type='radio']]:rounded-full peer-[&[type='radio']]:*:rounded-full">
      <div class="hidden size-full border border-primary2 bg-primary2" />
    </div>
  </div>
</template>
