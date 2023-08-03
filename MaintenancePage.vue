<script setup>
import { computed } from "vue";
import { useRouter } from "vue-router";

const iFrameSource = computed(
  () => "https://page.ctdmaintenancepage.workers.dev/"
); // mozda ovo da bude promenljiva?

const router = useRouter();

if (maintenanceFlag.value) {
  router.push({ name: "maintenance" });
}
</script>

<template>
  <div class="h-[calc(100vh-72px)] overflow-hidden">
    <iframe class="h-full w-full" :src="iFrameSource"></iframe>
  </div>
</template>
