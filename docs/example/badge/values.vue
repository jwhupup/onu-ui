<template>
  <div fscw gap-6>
    <OBadge o="primary" :value="99">
      <o-avatar class="o-gray dark-o-#3a3a3c" rounded />
    </OBadge>
    <OBadge o="primary" :value="100">
      <o-avatar class="o-gray dark-o-#3a3a3c" rounded />
    </OBadge>
    <OBadge :max="999" :value="199">
      <o-avatar class="o-gray dark-o-#3a3a3c" rounded />
    </OBadge>
    <OBadge :max="999" :value="1000">
      <o-avatar class="o-gray dark-o-#3a3a3c" rounded />
    </OBadge>
  </div>
</template>
