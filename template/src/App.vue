<template>
  <div id="app">
    <img class="logo" src="./assets/mm.jpg">
    {{#router}}
    <router-view/>
    {{else}}
    <HelloWorld/>
    {{/router}}
  </div>
</template>

<script>
{{#unless router}}
import index from './components/index'

{{/unless}}
export default {
  name: 'App'{{#router}}{{else}},
  components: {
    index
  }{{/router}}
}
</script>
<style lang="stylus" scoped>
@import 'common/stylus/variable'
#app
  width 100vw
  height 100vh
  text-align: center
  .logo
    width 200px
    margin-top: 200px
</style>
