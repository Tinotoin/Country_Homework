<template lang="html">
<div>
<ul>
  <list-item v-for="(country, index) in countries" :country="country" :key="index"></list-item>
</ul>
</div>
</template>

<script>
import ListItem from './ListItem.vue';

export default {
  name: 'countries-list',
  props: ['countries'],
  components: {
    "list-item": ListItem
  },
  //
  // data(){
  //   return{
  //     selectedCountry: null
  //   }
  // }
}
</script>

<style lang="css" scoped>
</style>
