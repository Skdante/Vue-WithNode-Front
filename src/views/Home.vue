<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>Login</h1>
    <form @submit.prevent="login(usuario)">
      <input type="email" placeholder="email" v-model="usuario.email">
      <input type="password" placeholder="password" v-model="usuario.password">
      <button type="submit">Acceder</button>
    </form>
  </div>
</template>

<script>
import {mapActions} from 'vuex'

export default {
  data() {
    return {
      usuario: {
        email: "",
        password: ""
      }
    }
  },
  methods: {
    ...mapActions(['login'])
  }
}
</script>
