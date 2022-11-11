<script setup lang="ts" name="OButton">
import { buttonProps } from './props'

const props = defineProps(buttonProps)
const slots = useSlots()
const isDisabled = computed(() => props.loading || props.disabled)
const onlyIcon = computed(() => slots.icon && !slots.default)
// const binds = Object.assign({}, useAttrs(), props.to ? { href: props.to } : {})
</script>

<template>
  <component
    :is="to ? 'a' : 'button'"
    :href="to"
    :type="to ? undefined : 'button'"
    :disabled="isDisabled"
    :aria-disabled="isDisabled"
    class="o-button o-button-base o-transition hover:o-button-hover active:o-button-active focus:o-button-focus"
    :class="[
      light ? 'o-button-light' : '',
      text ? 'o-button-text' : '',
      `o-${size}`,
      isDisabled ? 'o-disabled' : '',
      onlyIcon && 'aspect-square px-0',
    ]"
  >
    <div v-if="loading" i-carbon-circle-dash animate-spin />
    <slot v-else name="icon" />
    <slot />
  </component>
</template>
