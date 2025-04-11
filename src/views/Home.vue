<template>
    <div>
      <h1>Home Page</h1>
      HOMEPAGE
      <button @click="logout">Logout</button>
    </div>
  </template>
  
  <script>
  import { logoutUser } from '../composables/auth'
  
  export default {
    name: 'Home',
  
    methods: {
      async logout() {
        await logoutUser()
        this.$router.push('/login')
      }
    },
  
    mounted() {
      alert('Uspijeli smo')
    }
  }
  </script>
  