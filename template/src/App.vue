<template>
  <div id="app">
    <img src="./assets/mm.jpg">
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
@import 'common/stylus/mixin'
#app
  width 100vw
  height 100vh
  text-align: center
  .logo
    margin-top: 200px
</style>
