<script setup lang="ts">
import { storageDemo } from '~/logic/storage'

function openOptionsPage() {
  browser.runtime.openOptionsPage()
}
const openReminder = () => {
  browser.tabs.create({
    url: browser.runtime.getURL('dist/reminder/index.html'),
    active: true,
  })
}
</script>

<template>
  <main class="w-[300px] px-4 py-5 text-center text-gray-700">
    <Logo />
    <div>Popup</div>
    <SharedSubtitle />

    <button class="btn mt-2" @click="openOptionsPage">
wd      Open knOptions
    </button>
    <div class="mt-2">
      <span class="opacity-50">Storage:</span> {{ storageDemo }}
    </div>
    <button @click="openReminder">open reminder</button>
  </main>
</template>
