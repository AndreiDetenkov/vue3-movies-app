<script setup lang="ts">
type NavItem = {
  title: string
  url: string
}

defineProps<{
  item: NavItem
}>()
</script>

<template>
  <router-link
    :to="item.url"
    class="flex items-center justify-center text-center font-medium transition duration-300 ease-in-out hover:text-orange-600"
    active-class="text-orange-500 border-b-orange-500"
  >
    {{ item.title }}
  </router-link>
</template>
