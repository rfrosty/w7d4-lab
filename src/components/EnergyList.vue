<template lang="html">
  <div class="">
    <ul>
      <span>"I am an energy list"</span>
      <list-component></list-component>
    </ul>
  </div>
</template>

<script>

import ListComponent from './ListComponent.vue'

export default {
  name: 'energy-list',

  components: {
    "list-component": ListComponent
  }

}

</script>

<style lang="css" scoped>
</style>
