<template>
<div id="app" class="justify-center h-screen overflow-scroll flex md:flex-nowrap md:overflow-hidden flex-wrap gap-6">
  <SideBar/>
  <div class="flex flex-col gap-20">
  <Header />
  <TimeLine/>
  </div>
</div>
</template>

<script>

import SideBar from "@/components/SideBar.vue"
import TimeLine from "@/components/TimeLine.vue"
import Header from './components/Header.vue'
export default {
  name: 'CvA',
  components: {
    SideBar,
    TimeLine,
    Header
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color : #191c23;
  color: white;
  padding: 8px;
}
body {
  margin: 0;
  overflow: hidden;
}
</style>
