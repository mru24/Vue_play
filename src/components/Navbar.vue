<template>
  <div>
    <div class="container">
      <nav>
        <router-link :to="'/'">Home</router-link>
        <router-link :to="'/about'">About</router-link>
        <router-link :to="'/contact'">Contact</router-link>
      </nav>
      <div class="burger" @click="showNav=!showNav">

      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      showNav: false
    }
  },
  methods: {
    showNavbar: function () {
      var nav = document.querySelector('nav')
      console.log('ok')
      nav.style.top = 0
    }
  },
  created () {
    var vm = this
    if (vm.showNav) {
      vm.showNavbar()
    }
  }
}
</script>

<style lang="sass">

@import 'config'

nav
  margin: 30px 0
  @include bp-mobile
    position: absolute
    width: 70%
    top: -100%
  a, a:visited, a:active
    text-decoration: none
    color: #444
  a
    padding: 20px 40px
    margin: 5px
    background: #f5f5f5
    border-radius: 4px
    transition: .4s
    float: left
    &:hover
      background: #fff
    &:last-child
      background: #eee
      float: right
    @include bp-mobile
      clear: both
      width: 100%
      margin: 0
  .router-link-exact-active
    border-bottom: 4px solid #078717

.burger
  position: fixed
  top: 10px
  right: 10px
  width: 50px
  height: 50px
  background: red
  display: none
  @include bp-mobile
    display: block
</style>
