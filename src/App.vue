<template>
  <div id="app">
    <BaseSpinner/>
    <button @click="mostrarSpinner()">Mostrar Spinner</button>
    <!-- <router-view/> -->
  </div>
</template>

<script>
import BaseSpinner from './components/global/BaseSpinner'

export default {
  components: {
    BaseSpinner
  },
  methods: {
    mostrarSpinner(){
      this.$root.$emit('Spinner::show')
    }
  }
}
</script>

<style lang="scss">

</style>
