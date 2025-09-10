<script setup>
import badge from './Badge.vue'
</script>

<template>
  <div class="p-6 space-y-3">
    <badge status="Active"/>
    <badge status="Paid"/>
    <badge status="UnPaid"/>
    <badge status="Error"/>
    <badge status="InActive"/>
  </div>
</template>

<style  scoped>
</style>
