<template>
  <div class="o-cols"
  :class="[ itemsModifier, gutterModifier ]">
    <slot></slot>
  </div>
</template>

<script lang="">
  export default {
    props: [
      {
        name: 'verticalAlign',
        type: [ String, Boolean ],
        default: false
      }, {
        name: 'gutter',
        type: [ Number, String, Boolean ],
        default: false
      }
    ],
    computed: {
      verticalAlignModifier () {
        if (this.verticalAlign) {
          return `o-cols--${$this.verticalAlign}`
        }
        return ''
      },
      gutterModifier () {
        if (this.gutter) {
          return `o-cols--gutter-${this.gutter}`
        }
        return ''
      }
    }
  }
</script>
