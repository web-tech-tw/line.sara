<template>
  <button
    class="-m-3 p-3 flex w-full items-center rounded-md text-gray-900 hover:text-gray-700"
    type="button"
  >
    <dynamic-hero-icon
      v-if="props.icon"
      :name="props.icon"
      class="rounded-full w-6 h-6 mr-4"
    />
    <slot name="prepend" />
    <div class="text-left">
      <div class="text-base font-medium">
        {{ props.name }}
      </div>
      <div class="mt-1 text-sm">
        {{ props.description }}
      </div>
    </div>
  </button>
</template>

<script setup>
import DynamicHeroIcon from "./DynamicHeroIcon.vue"

const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  icon: {
    type: String,
    required: false,
    default: () => "",
  },
});
</script>
