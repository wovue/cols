<template>
  <div class="o-cols__col"
  :class="[ sizeModifier, responsiveModifier, xsModifier, smModifier, mdModifier, lgModifier, xlModifier ]">
    <slot></slot>
  </div>
</template>

<script lang="">
  export default {
    props: [
      {
        name: 'size',
        type: [ Number, String, Boolean ],
        default: false
      }, {
        name: 'responsive',
        type: [ Object, Boolean ],
        default: false
      }, {
        name: 'xs',
        type: [ Number, String, Boolean ],
        default: false
      }, {
        name: 'sm',
        type: [ Number, String, Boolean ],
        default: false
      }, {
        name: 'md',
        type: [ Number, String, Boolean ],
        default: false
      }, {
        name: 'lg',
        type: [ Number, String, Boolean ],
        default: false
      }, {
        name: 'xl',
        type: [ Number, String, Boolean ],
        default: false
      }
    ],
    computed: {
      sizeModifier () {
        if (this.size) {
          return `o-cols__col--${this.size}`
        }
        return ''
      },
      responsiveModifier () {
        if (this.responsive) {
          let responsive = this.responsive
          let responsiveModifier = ''

          for (let key in responsive) {
            if (responsive.hasOwnProperty(key)) {
              responsiveModifier += `o-cols__col--${responsive[key]}@${key} `
            }
          }

          return responsiveModifier
        }
        return ''
      },
      xsModifier () {
        if (this.xs) {
          return `o-cols__col--${this.xs}@xs`
        }
        return ''
      },
      smModifier () {
        if (this.sm) {
          return `o-cols__col--${this.sm}@sm`
        }
        return ''
      },
      mdModifier () {
        if (this.md) {
          return `o-cols__col--${this.md}@md`
        }
        return ''
      },
      lgModifier () {
        if (this.lg) {
          return `o-cols__col--${this.lg}@lg`
        }
        return ''
      },
      xlModifier () {
        if (this.xl) {
          return `o-cols__col--${this.xl}@xl`
        }
        return ''
      }
    }
  }
</script>
