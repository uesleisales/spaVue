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
  name: 'App',
  components: {
    BaseSpinner
  },
  methods: {
    mostrarSpinner(){
      this.$root.$emit('Spinner::show')
    }
  },
  mounted (){
    console.log(this.$firebase)
  }
}
</script>

<style lang="scss">
#app{
  min-height: 100vh;
  background: var(--darker);
}
</style>
