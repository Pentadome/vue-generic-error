<script setup lang="ts" generic="T">
defineProps<{
  type: T;
}>();

defineModel<boolean>({ required: true });
</script>