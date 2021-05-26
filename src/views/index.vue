<template>
  <div class="about">

  </div>
</template>
<script>
import { defineComponent,ref,onMounted } from 'vue';
export default defineComponent({
  name:'Index',
  setup(){
    const testValue = ref(null);
    const ass = ref(null);
    onMounted(() => {
      // console.log(123)
    })
    const getRef = () => {
      console.log(ass.value)
    }
    return {
      testValue,
      ass,
      getRef
    }
  }
})
</script>
<style lang="scss">

</style>
