<script lang="ts" setup>
const online = useOnline()
</script>

<template>
  <div h-full w-full flex flex-col items-center justify-center>
    <div flex items-center py-2>
      <span mx-2>网络状态</span>
      <span mx-2>{{ online ? '在线' : '离线' }}</span>
    </div>
    <main min-h-0 w-full flex-1 overflow-visible>
      <slot />
    </main>
  </div>
</template>
