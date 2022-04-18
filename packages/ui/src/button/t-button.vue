<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script lang="ts">
import {defineComponent, PropType} from '@vue/composition-api'

type Size = 'sm' | 'md' | 'lg'

export default defineComponent({
  name: "t-button",
  props: {
    size: {
      type: String as PropType<Size>,
      default: 'md'
    }
  }
})
</script>

<style>
.btn {
  background: red;
  padding: 4px;
}
</style>
