<template>
<NavBarComp/>
<router-view/>
</template>

<script>
import NavBarComp from './components/NavBar-comp.vue'

export default {

components: {NavBarComp}
  //  data() {
  //   return { message: "Hello There", isRed: true, color: 'green' };
  // },

  // methods: {
  //   toggleRed() {
  //     this.isRed = !this.isRed
  //   },
  //   toggleColor () {
  //     this.color= this.color === 'green' ? 'blue' : 'green'
  //   }
  // }

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
