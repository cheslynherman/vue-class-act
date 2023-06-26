<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view />
  

  <p><span :title="message">Hover & See the Dynamic Title</span></p>
  <p :class="{ red: isRed }" @click="toggleRed()">
    This should be red... But click me to toggle
  </p>
  <p :style="{ color }" @click="toggleColor()">
    This will change color when clicking
  </p>
</template>

<script>
export default {
   data() {
    return { message: "Hello There", isRed: true, color: 'green' };
  },

  methods: {
    toggleRed() {
      this.isRed = !this.isRed
    },
    toggleColor () {
      this.color= this.color === 'green' ? 'blue' : 'green'
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

 .red {
    color: red;
  }

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
