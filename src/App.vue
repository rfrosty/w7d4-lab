<template lang="html">
<div class="">
  <p>Hello World</p>
  <span>{{ data }}</span>
  <!-- <energy-list></energy-list> -->
</div>
</template>

<script>

// import EnergyList from './components/energy'

export default {
  name: 'app',

  data() {
    return {
      data: [],
      selectedData: null
    }
  },


  mounted () {
    fetch('https://api.carbonintensity.org.uk/generation')
    .then(response => response.json())
    .then(one => one.data)
    .then(two => two.generationmix)
    // .then(three => three[0])
    .then(data => this.data = data)

  },

}
</script>

<style lang="css" scoped>
</style>
