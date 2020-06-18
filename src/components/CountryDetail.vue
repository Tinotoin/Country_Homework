<template lang="html">
<div class="sub-container">

  <div v-if='country'>
    <h3>{{country.name}}</h3>
    <p>Population: {{country.population}}</p>
    <p>Region: {{country.region}}</p>
    <img class="med-flag" :src="country.flag"/>
  </div>
</div>

</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>

.sub-container {
  display: flex;
  align-content: center;
}

.med-flag {
  height: 50px;
}
</style>
