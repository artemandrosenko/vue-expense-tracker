<template>
  <h4>Your Balance</h4>
  <h2 id="balance">${{ total }}</h2>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  total: {
    type: Number,
    required: true,
  }
});

</script>
