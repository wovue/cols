# Cols

The `wovue-cols` module contains the grid system components.

Install using npm:  

```sh
$ npm install --save wovue-cols
```

**Note** this will only works with `webpack` build system.

**Note** The `wv-cols` component use negative margins, you will need a root element overflowing the `wv-cols` component, or it will cause horizontal scroll.

## Usage

```js
require('wovue-cols/src/_components.cols.scss')

import { WvCols, WvCol } from 'wovue-cols'

new Vue({
  components: {
    WvCols,
    WvCol
  }
})
```

```html
<div class="u-overflow-hidden">
  <wv-cols :gutter="4" vertical-align="middle">
    <wv-col size="6" md="2" lg="8">
      <!-- here your content -->
    </wv-col>
    <wv-col size="6" md="10" lg="4">
      <!-- here your content -->
    </wv-col>
    <wv-col size="12">
      <wv-cols :gutter="2">
        <wv-col size="3">
          <!-- here your content -->
        </wv-col>
        <wv-col size="7">
          <!-- here your content -->
        </wv-col>
      </wv-cols>
    </wv-col>
  </wv-cols>
</div>
```

### Props

#### cols

| Name | Type | Default | Description |
|------|------|---------|-------------|
| verticalAlign | String, Boolean | `false` | Colums vertical align. The support values are `'middle'` and `'stretch'` |
| gutter | Number, String, Boolean | `false` | Alter spacing between colums. The support values are `1`, `2`, `3`, `4`, `5`, `6` |

#### col

| Name | Type | Default | Description |
|------|------|---------|-------------|
| size | Number, String, Boolean | `false` | Column size. The support values are `'auto'`, `'fit'`, `1`, `2`, `3`, ...`12` |
| responsive | Object, Boolean | `false` | Custom breakpoints and values. |
| xs | Number, String, Boolean | `false` | Column size for xs devices. The support values are `'auto'`, `'fit'`, `1`, `2`, `3`, ...`12` |
| sm | Number, String, Boolean | `false` | As above. |
| md | Number, String, Boolean | `false` | As above. |
| lg | Number, String, Boolean | `false` | As above. |
| xl | Number, String, Boolean | `false` | As above. |

### Breakpoints

| Key | Value |
|-----|-------|
| xs | `320px` |
| sm | `480px` |
| md | `768px` |
| lg | `992px` |
| xl | `1200px` |
