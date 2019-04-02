<template>
  <div class="about">
    <h1>This is an about page</h1>
    <SignUp/>
  </div>
</template>

<script>
import SignUp from "../components/forms/SignUp.vue";
export default {
  name: "signup",
  components: {
    SignUp
  }
};
</script>