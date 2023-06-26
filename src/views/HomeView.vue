<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>

  <!-- <div>
    <p v-if="hours<12">Good morning!</p>
    <p v-if="hours>=12 && hours < 18">Good Afternoon!</p>
    <p v-if="hours >=18">Good Evening!</p>
  </div> -->

  <!-- <div>
    <p v-if="path === '/'">You are on the Home Page</p>
    <p v-else>Youre on {{path}}</p>
  </div> -->

  <p><span :title="message">Hover & See the Dynamic Title</span></p>
  <p :class="{ red: isRed }" @click="toggleRed()">
    This should be red... But click me to toggle
  </p>
  <p :style="{ color }" @click="toggleColor()">
    This will change color when clicking
  </p>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

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

};

</script>

<style>
.red {
    color: red;
  }
</style>
