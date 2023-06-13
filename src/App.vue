<template>

  <TugasBootstrap />
  <!-- <HomeBootstrap /> -->
  <HomeAku />
  <h1>Nama saya adalah {{ nama }}</h1>
  <h1>Umur saya adalah {{ umur }}</h1>
  <h1>{{ bilangan }}</h1>
  <button v-on:click="kali">Kali</button>
  <button v-on:click="kurang">Kurang</button>
  <button v-on:click="tambah">Tambah</button>
  <button v-on:click="bagi">Bagi</button>
</template>

<script>
import HomeAku from "./components/HomeAku.vue";
import TugasBootstrap from "./components/TugasBootstrap.vue";
// import HomeBootstrap from "./components/HomeBootstrap.vue";

// import HelloWorld from './components/HelloWorld.vue'
// import HomeDua from './components/HomeDua.vue'

export default {
  name: "App",
  data() {
    return {
      nama: "aldi Taher",
      umur: 20,
      bilangan: 1,
    };
  },
  components: {
    HomeAku,
    TugasBootstrap,
  },
  methods: {
    tambah() {
      this.bilangan += 1;
    },
    kurang() {
      this.bilangan -= 1;
    },
    kali() {
      this.bilangan *= 10;
    },
    bagi() {
      this.bilangan /= 10;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
