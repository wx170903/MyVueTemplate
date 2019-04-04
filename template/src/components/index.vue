<template>
  <div class="hello">
    {{msg}}
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'template'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
@import '~common/stylus/variable'
</style>
