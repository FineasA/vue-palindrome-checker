<template>
  <div class="container">
    <title-heading></title-heading>
    <palindrome-checker></palindrome-checker>
  </div>
</template>

<script>
import TitleHeading from "./components/TitleHeading.vue";
import PalindromeChecker from "./components/PalindromeChecker.vue";
export default {
  components: {
    TitleHeading,
    PalindromeChecker
  }
};
</script>

<style>
.container {
  padding: 150px;
  border: 2px solid aliceblue;
  border-radius: 15px;
  margin-top: 12.5%;
}
</style>