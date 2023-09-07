<script setup>
import { ref } from "vue";

const props = defineProps({
  mainValue: {
    type: String,
    default: "",
  },
});

const value = ref(props.mainValue);
</script>

<template>
  <input
    v-model="value"
    type="text"
    class="search"
    @keyup.enter="$emit('enter', value)"
  />
</template>