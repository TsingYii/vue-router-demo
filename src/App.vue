<template>
  <div id="app">
    <layout />
  </div>
</template>

<script>
import layout from '@/views/layout'
export default {
  name: 'App',
  components: {
    layout
  }
}
</script>

<style>
 html,body,#app{
   height: 100%;
   width: 100%;
   background: orange;
 }

 *{
   padding: 0;
   margin: 0;
 }

</style>
