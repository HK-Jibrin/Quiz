<template>
  <div class="quiz">
    <div class="answers-container">
      <h3>Thank you for playing!</h3>
      <p>
        You scored
        <span>{{numCorrect}}/{{numTotal}}</span>
      </p>
      <div class="buttons">
        <router-link class="button" to="/question">Play Again</router-link>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  computed: {
    ...mapGetters(["numCorrect", "numTotal"])
  }
};
</script>

<style scoped>
.answers-container {
  padding: 20px;
}
.answers-container p {
  margin-top: 20px;
  font-size: 1.1em;
  text-align: center;
  color: whitesmoke;
}
.answers-container p span {
  font-weight: bolder;
}
.buttons {
  display: flex;
  flex-direction: column;
  width: 50%;
  height: 100%;
  border: none !important;
  justify-content: center;
  align-items: center;
}
.buttons .button {
  margin-top: 10px;
  width: 50px;
  text-decoration: none;
  text-align: center;
  color: #fff;
  background: #3dc988;
  padding: 15px;
  font-size: 1em;
  border-radius: 20px;
}
.button:hover {
  background: #a7aac9;
}
</style>