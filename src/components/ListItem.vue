<template lang="html">
<!-- <select v-model="selectedCountry"> -->
  <!-- <option disabled value="">Select a Country</option>
  <option v-for="country in countries">{{country.name}}</option> -->
<li v-on:click="handleClick">{{country.name}}</li>
</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: 'list-item',
  props: ['country'],
  methods: {
      handleClick(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}

</script>

<style lang="css" scoped>
</style>
