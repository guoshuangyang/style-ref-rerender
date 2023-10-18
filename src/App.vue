<script setup>
import { ref } from 'vue';
const testValue = ref('10px');
setInterval(() => {
  testValue.value = Math.random() * 80 + 'px';
}, 500);
</script>
//
<script>
// export default {
//   data() {
//     return {
//       testValue1: '20px',
//     };
//   },
//   mounted() {
//     setInterval(() => {
//       this.testValue1 = Math.random() * 80 + 'px';
//     }, 200);
//   },
// };
//
</script>
<template>
  <div
    :style="{
      padding: testValue,
    }"
  >
    {{ new Date().toLocaleString() }}
  </div>
  <!-- <div
    :style="{
      padding: testValue1,
    }"
  >
    {{ new Date().toLocaleString() }}
  </div> -->
</template>
