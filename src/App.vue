<template>
  <NavHeader/>
  <router-view />
</template>
<script>
import NavHeader from './components/NavHeader'
export default{
  components:{NavHeader}
}
</script>
<style lang="scss">
#app {
  font-family: Roboto, Helvetica, Arial, sans-serif;
}
</style>
