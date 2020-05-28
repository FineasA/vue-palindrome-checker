<template>
  <div class="palindrome-container">
    <b-form-input
      class="user-input-field"
      size="lg"
      v-model="userInput"
      placeholder="Enter text to check..."
    ></b-form-input>
    <h3 class="mt-2 result">Palindrome : {{isPalindrome}}</h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isPalindrome: false,
      userInput: "",

      userInputReverse: ""
    };
  },
  methods: {
    checkPalindrome() {
      this.userInputReverse = this.userInput
        .split("")
        .reverse()
        .join("");

      if (
        this.userInputReverse.toLowerCase() === this.userInput.toLowerCase()
      ) {
        console.log("PALINDROME!!!!!!!");
        this.isPalindrome = true;
      } else {
        this.isPalindrome = false;
      }
    }
  },
  updated() {
    this.checkPalindrome();
  }
};
</script>

<style>
.result {
  padding-top: 1.2rem;
  opacity: 65%;
}

.palindrome-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.user-input-field {
  margin: 2.2rem;
  width: 550px;
}
</style>