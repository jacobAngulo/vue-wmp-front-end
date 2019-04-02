<template>
  <form v-on:submit="signUp">
    <input type="text" v-model="username" placeholder="username">
    <input type="password" v-model="password" placeholder="password">
    <input type="password" v-model="confirmPassword" placeholder="confirm password">
    <input type="submit" value="sign up">
  </form>
</template>

<script>
export default {
  name: "SignUp",
  data() {
    return {
      username: "",
      password: "",
      confirmPassword: ""
    };
  },
  methods: {
    signUp(e) {
      e.preventDefault();
      if (this.username && this.password) {
        if (this.password === this.confirmPassword) {
          console.log({
            username: this.username,
            password: this.password
          });
        } else {
          alert("your passwords do not match");
        }
      } else {
        alert("all fields must be filled out");
      }
    }
  }
};
</script>

<style>
</style>
