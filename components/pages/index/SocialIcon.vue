<template>
  <li
    class="p-2 border-2 rounded-full border-darkGray-300 bg-darkGray-500 focus-within:border-primary-500"
  >
    <a
      :href="href"
      class="focus:outline-none group"
      target="_blank"
      rel="noopener"
      :title="title"
    >
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
        class="w-6 h-6 transition-colors icon group-hover:text-primary-400"
        :aria-label="`${title} icon`"
      >
        <slot />
      </svg>
    </a>
  </li>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: () => null,
    },

    href: {
      type: String,
      default: () => null,
    },
  },
}
</script>
