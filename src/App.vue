<template lang="pug">
  v-app
    login-page
    
  
</template>

<script>
import LoginPage from "./components/LoginPage";

export default {
  name: "App",

  components: {
    LoginPage,
  },

  data: () => ({
    //
  }),
};
</script>
