<template>
  <div id="app" style="height:100%" >
    <layout> 
      <router-view></router-view>
    </layout>
  </div>
</template>
<script>
export default {
  components: {
    layout: ()=> import('@/layout/layout.vue')
  }
}
</script>
