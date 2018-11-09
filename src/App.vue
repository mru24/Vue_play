<template>
  <div id="app">
    <Navbar />
    <div class="clearFloat"></div>
    <transition mode="out-in">
      <router-view/>
    </transition>
    <footer>
      WW Project Studio &copy; 2018
    </footer>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
export default {
  components: {
    Navbar
  }
}
</script>

<style lang="sass">
@import './components/config'

footer
  position: fixed
  bottom: 10px
  left: 50%
  transform: translateX(-50%)

.v-leave-active, .v-enter-active
  transition: all 1s ease-out
.v-leave-to
  opacity: 0
  transform: translateX(-100%)
.v-enter
  opacity: 0
  transform: translateX(100%)

</style>
