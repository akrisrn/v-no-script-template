<template>
  <div id="hello-world" v-html="html"></div>
</template>

<script lang="ts">
  @vno.VPD.Component({
    el: '#hello-world',
  })
  export default class HelloWorld extends vno.Vue {
    get html() {
      return vno.markdown.renderMD(`## This's a v-no page component!

Recommend to use [\`vue-class-component\`](https://github.com/vuejs/vue-class-component) with TypeScript and SCSS.

\`vno.VDP\` is an alias of [\`vue-property-decorator\`](https://github.com/kaorun343/vue-property-decorator), and \`vno.Vue\` is an alias of \`vno.VDP.Vue\`.`);
    }
  }
</script>

<style lang="scss" scoped>
  #hello-world {
    border-left: 6px solid rgba(var(--info-color), 0.5);
    padding-left: 16px;
  }
</style>
