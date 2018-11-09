<template>
  <div class="contact">
    <div class="container">
      <h1>Contact Us</h1>
      <h4>Lorem ipsum dolor sit amet.</h4>
      <div class="formContainer">
        <h4>Sign up for our newsletter</h4>
        <form>
          <div class="formControl">
            <label>Name</label>
            <input type="text">
          </div>
          <div class="formControl">
            <label>Email</label>
            <input type="text">
          </div>
          <button type="submit">Subscribe</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      show: false
    }
  }
}
</script>

<style lang="sass" scoped>

$borderCol: #333
$darkBg: #120a0a
$borderFt: 4px solid white
$borderLt: 1px solid $borderCol
$radius: 4px

.formContainer
  margin: 40px 0
  padding: 10px
  background: $darkBg
  color: white
  border-radius: $radius
  form
    padding: 40px 30px
    font-weight: 200
    border: 1px solid $borderCol
    border-radius: $radius
    label, input
      display: block
      width: 100%
      margin-bottom: 15px
    label
      color: #f5f5f5
    input
      height: 35px
      background: transparent
      color: #fff
      font-size: 18px
      padding-left: 20px
      border: none
      border-radius: $radius
      border-left: $borderFt
      border-right: $borderFt
      border-top: $borderLt
      border-bottom: $borderLt
      transition: .6s
      &:hover, &:focus
        background: #222
    button
      display: block
      margin: auto
      margin-top: 40px
      padding: 10px
      width: 100%
      border: none
      border-radius: $radius
      border-left: $borderFt
      border-right: $borderFt
      background: $darkBg
      color: white
      cursor: pointer
      transition: .6s
      &:hover
        background: #11a124

</style>
