<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <!-- <li class="minus">Cash
        <span>-100</span>
        <button class="delete-btn">x</button>
    </li>
    <li class="plus">Salary
        <span>2400</span>
        <button class="delete-btn">x</button>
    </li> -->
    <li
      v-for="transaction in transactions"
      v-bind:key="transaction.id"
      v-bind:class="transaction.amount < 0 ? 'minus' : 'plus'"
    >
      {{ transaction.text }} <span>${{ transaction.amount }}</span>
      <button class="delete-btn" @click="deleteTransaction(transaction.id)">x</button>
    </li>
  </ul>
</template>

<script setup>
import { defineProps } from 'vue'

const emit = defineEmits(['transactionDeleted'])

const props = defineProps({
  transactions: {
    type: Array,
    required: true,
  }
});

const deleteTransaction = (transactionId) => {
  emit('transactionDeleted', transactionId);

}
</script>
