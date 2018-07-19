<template>
  <div id="app">
    <router-link to="/foo" @click="onFoo()">Go to Foo</router-link>
    <router-link to="/bar" @click="onBar()">Go to Bar</router-link>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods:{
    onBar:function(){
      this.$router.go({path : '/bar'})
    },
    onFoo:function(){
        this.$router.go({path : '/foo'})
    }
  }
}
</script>

<style>
#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
