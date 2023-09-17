<script setup lang="ts">
import { storageDemo } from '~/logic/storage'
import { useStorage } from '@vueuse/core'

const otherstorageDemo = useStorage('webext-demo')

function openOptionsPage() {
  browser.runtime.openOptionsPage()
}
</script>

<template>
  <main class="w-[300px] px-4 py-5 text-center text-gray-700">
    {{  storageDemo }}
    {{  otherstorageDemo }}
  </main>
</template>
