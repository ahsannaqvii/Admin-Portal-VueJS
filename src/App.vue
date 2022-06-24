<template>
  <div id="inspire">
    <Sidebar  />
    <TopBar/>
  </div>  
</template>
<script>
import Sidebar from "./components/SideBar";
import TopBar from "./components/TopBar";

export default {
  name: "App",
  components: { TopBar,Sidebar },
  data: () => ({
    cards: ["Today", "Yesterday"],
  }),
  methods: {},
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
