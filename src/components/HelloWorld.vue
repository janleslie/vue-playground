<template>
  <h2>{{ msg }}</h2>
  <button @click="increment" class="flex border items-center px-2 py-1 rounded">
    <span class="i-ph-address-book-thin w-5 h-5" />
    <span class="h-7 pl-1">count is: {{ count }}</span>
  </button>
</template>

<script setup lang="ts">
const store = useStore();
const count = computed(() => store.count);
type Props = {
  msg: string;
  optionalProp?: number;
};
defineProps<Props>();

const increment = () => {
  store.increment();
};
</script>
