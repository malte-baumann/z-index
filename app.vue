<template>
  <div>
    <UModal description="Select z-index">
      <UButton label="Open Modal" class="m-8"/>
      <template #content>
        <USelect :items="['One', 'Two', 'Three']" class="w-64 my-4" />
        <UDropdownMenu :items="items" :content="{
          align: 'start',
          side: 'bottom',
          sideOffset: 8
        }" class="w-48">
          <UButton label="Open" icon="i-heroicons-bars-3" color="neutral" variant="outline" class="my-4"/>
        </UDropdownMenu>
        <UInputMenu v-model="value" :items="input_items" class="my-4"/>
      </template>
    </UModal>

    <UDrawer description="Select z-index">
      <UButton label="Open Drawer" class="m-8"/>
      <template #content>
        <USelect :items="['One', 'Two', 'Three']" class="w-64 my-4" />
        <UDropdownMenu :items="items" :content="{
          align: 'start',
          side: 'bottom',
          sideOffset: 8
        }" class="w-48">
          <UButton label="Open" icon="i-heroicons-bars-3" color="neutral" variant="outline" class="my-4"/>
        </UDropdownMenu>
        <UInputMenu v-model="value" :items="input_items" class="my-4"/>
      </template>
    </UDrawer>

    <USlideover description="Select z-index">
      <UButton label="Open Slideover" class="m-8"/>
      <template #content>
        <USelect :items="['One', 'Two', 'Three']" class="w-64 my-4" />
        <UDropdownMenu :items="items" :content="{
          align: 'start',
          side: 'bottom',
          sideOffset: 8
        }" class="w-48">
          <UButton label="Open" icon="i-heroicons-bars-3" color="neutral" variant="outline" class="my-4"/>
        </UDropdownMenu>
        <UInputMenu v-model="value" :items="input_items" class="my-4"/>
      </template>
    </USlideover>
  </div>
</template>
<script setup lang="ts">
const items = ref([
  {
    label: 'Profile',
    icon: 'i-heroicons-user'
  },
  {
    label: 'Billing',
    icon: 'i-heroicons-credit-card'
  },
  {
    label: 'Settings',
    icon: 'i-heroicons-cog'
  }
])
const input_items = ref([
  ['Apple', 'Banana', 'Blueberry', 'Grapes', 'Pineapple'],
  ['Aubergine', 'Broccoli', 'Carrot', 'Courgette', 'Leek']
])
const value = ref('Apple')
</script>
<style>
@import "tailwindcss";
@import "@nuxt/ui";
</style>