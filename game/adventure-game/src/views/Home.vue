<template>
  <div class="home">
    <h1>Welcome to the Adventure Game</h1>
    <p>Your journey begins here...</p>
    <button @click="startGame">Start Game</button>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
  },
  methods: {
    startGame() {
      this.$router.push({ name: 'Game' });
    },  
  }
}
</script>

<style scoped>
.home {
  color: white;
  background-color: midnightblue;
  text-align: center;
  padding: 20px;
}
</style>