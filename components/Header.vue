<template>
    <header class="flex items-center justify-between p-4 bg-gray-100 dark:bg-gray-800">
      <div class="flex items-center gap-4">
        <ShieldIcon class="w-6 h-6" />
        <span class="text-lg font-semibold">MITRE Attack Analyzer</span>
      </div>
      <div class="flex items-center gap-4">
        <Button variant="outline">
          Menu
        </Button>

      </div>
    </header>
  </template>

<script>
import ShieldIcon from '@/components/ShieldIcon.vue'
import Button from '@/components/Button.vue'

export default {
  components: {
    ShieldIcon,
    Button,
  }
}
</script>

<style scoped>
/* Your styles here */
</style>