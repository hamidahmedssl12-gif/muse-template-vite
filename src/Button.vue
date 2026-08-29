<script setup>
defineProps({
  label: { type: String, default: 'Click me' },
  disabled: { type: Boolean, default: false },
  variant: { type: String, default: 'primary' },
})
</script>

<template>
  <button :disabled="disabled" :class="['btn', variant]">{{ label }}</button>
</template>

<style scoped>
.btn {
  padding: 8px 16px;
  border-radius: 6px;
  border: none;
  font-weight: 500;
  cursor: pointer;
}
.btn.primary {
  background: #4f46e5;
  color: #fff;
}
.btn.secondary {
  background: #e5e7eb;
  color: #111;
}
.btn:disabled {
  opacity: 0.5;
  cursor: default;
}
</style>
