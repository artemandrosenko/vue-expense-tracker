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
    </li>
  </ul>
</template>

<!-- <script>
export default {
  // data() {
  //   return {
  //     transactions: [
  //       { id: 1, text: 'Flower', amount: -19.99 },
  //       { id: 2, text: 'Salary', amount: 2400.99 },
  //       { id: 3, text: 'Book', amount: -10 },
  //       { id: 4, text: 'Camera', amount: 150 },
  //     ],
  //   };
  // },

  setup() {
    const transactions = [
      { id: 1, text: 'Flower', amount: -19.99 },
      { id: 2, text: 'Salary', amount: 2400.99 },
      { id: 3, text: 'Book', amount: -10 },
      { id: 4, text: 'Camera', amount: 150 }
    ];

    return {
      transactions,
    };
  }
}
</script> -->

<script setup>
const transactions = [
  { id: 1, text: 'Flower', amount: -19.99 },
  { id: 2, text: 'Salary', amount: 2400.99 },
  { id: 3, text: 'Book', amount: -10 },
  { id: 4, text: 'Camera', amount: 150 }
];
</script>
