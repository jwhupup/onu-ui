<script setup lang="ts">
const mv = ref(true)
const toggleDisabled = ref(true)
</script>

<template>
  <div space-y-2>
    <div fscw gap-2>
      <span text-primary>Toggle those disabled:</span> <o-switch v-model="toggleDisabled" o="error" />
    </div>
    <div fscw gap-2>
      <o-switch v-model="mv" :disabled="toggleDisabled" o="primary" />
      <o-switch v-model="mv" :disabled="toggleDisabled" v o="secondary" />
      <o-switch v-model="mv" :disabled="toggleDisabled" o="success" />
      <o-switch v-model="mv" :disabled="toggleDisabled" o="warning" />
      <o-switch v-model="mv" :disabled="toggleDisabled" o="error" />
      <o-switch v-model="mv" :disabled="toggleDisabled" o="info" />
    </div>
  </div>
</template>
