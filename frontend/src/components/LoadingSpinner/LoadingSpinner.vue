<script setup lang="ts">
defineProps<{
  isShow: boolean;
}>();
</script>

<template>
  <Transition name="fade">
    <div v-if="isShow" class="loading-spinner">
      <p class="loading-text">如无法正常加载，请更换浏览器打开</p>
    </div>
  </Transition>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 2.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.loading-spinner {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.loading-text {
  font-size: 16px;
  color: #000;
}

</style>
