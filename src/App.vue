<template>
  <div id="nav">
    <el-button @click="open">Home</el-button> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/>
</template>

<script>
import { defineComponent } from 'vue'
export default defineComponent({
  methods: {
    open() {
      this.$message.success('Home')
    }
  }
})
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
