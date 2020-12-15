<template>
  <div>
    <nav>
      <p><router-link :to="{ name: 'Home' }">Home</router-link></p>
      <p><router-link :to="{ name: 'About' }">About</router-link></p>
      <p>User Profile</p>
    </nav>
    <div>
      <span v-for="(id, index) in userIds" :key="index">
        <router-link :to="{ name: 'ViewProfile', params: {user_id: id}}"
        >Profile {{ id }}</router-link>
      </span>
      <button @click="goBack">Go Back</button>
      <button @click="goHome">Go Home</button>
      <button @click="goForward">Go Forward</button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Navbar',
    data() {
      return {
        userIds: ['1', '2', '3', '4']
      }
    },
    methods: {
      goHome(){
        this.$router.push({ name: 'Home' })
      },
      goBack(){
        this.$router.go(-1)
      },
      goForward(){
        this.$router.go(1)
      }
    }
  }
</script>

<style scoped>
  nav {
    /* background: lightgrey; */
    padding: 1rem;
    display: flex;
    justify-content: space-around;
  }

  nav a {

  }

  div span a {
    margin: 0 .5rem;
  }

  a.router-link-exact-active {
    color: purple;
    background: yellow;
  }
</style>
