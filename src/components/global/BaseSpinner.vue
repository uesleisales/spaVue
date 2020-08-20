<template>
    <div class="base-apinner fa-3x" v-if="visible">
        <i class="fas fa-circle-notch fa-spin"></i>
    </div>
</template>

<script>
export default {
    data(){
        return {
            visible: false,
        }
    },
    created : function (){
        this.$root.$on('Spinner::show', this.alternarSpinner)

        this.$root.$on('Spinner::hide', this.alternarSpinner)
    },

    methods: {
    alternarSpinner(){
      this.visible = !this.visible
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/variables';

.base-apinner{
    top: 0;
    bottom: 0;
    right: 0;
    position: absolute;
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: $dark-medium;
    color: $featured;
    z-index: 99999;
}
</style>