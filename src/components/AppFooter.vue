<template>
  <footer class="mt-16 pb-16 text-sm leading-6">
    <div class="max-w-7xl mx-auto mt-11 divide-y divide-gray-200 px-4 sm:px-6 md:px-8">
      「meJob 咪價」是一個自由的工作機會平台。
    </div>
    <div class="max-w-7xl mx-auto mt-5 divide-y divide-gray-200 px-4 sm:px-6 md:px-8 text-sky-700">
      <a
        class="mr-3"
        href="https://github.com/web-tech-tw/mejob"
      >網站原始碼</a>
      <a
        class="mr-3"
        href="https://web-tech.tw/#/privacy"
      >隱私權政策</a>
    </div>
    <div class="max-w-7xl mx-auto mt-5 divide-y divide-gray-200 px-4 sm:px-6 md:px-8">
      &copy; {{ year }}
      <a
        class="ml-1 hover:text-slate-900"
        :href="homeInteHost"
      >
        臺灣網際網路技術推廣組織
        Taiwan Web Technology Promotion Organization (Web Tech TW)
      </a>
    </div>
  </footer>
</template>

<script setup>
const homeInteHost = import.meta.env.VITE_HOME_INTE_HOST;
const year = new Date().getFullYear();
</script>
