<!--
 * @Author: Ena by15242952083@outlook.com
 * @Date: 2024-11-13 23:28:18
 * @LastEditors: Ena by15242952083@outlook.com
 * @LastEditTime: 2024-11-13 23:33:46
 * @FilePath: \mask-issues\app\components\Issues\Mask.vue
 * @Description:
 * Copyright (c) 2024 by ${git_name} email: ${git_email}, All Rights Reserved.
-->
<script setup lang="ts">
const maskRef = ref()
const { width, height } = useElementSize(maskRef)
</script>

<template>
  <div class="mask-box" h-400px w-200px>
    <div ref="maskRef" class="mask" />
    <div h-50px w-200px flex flex-col items-center justify-center>
      <span>元素宽度: {{ width }}</span>
      <span>元素高度: {{ height }}</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.mask-box {
  .mask {
    height: 350px;
    width: 200px;
    background: #57606f;
    mask-image: radial-gradient(circle, rgba(0, 0, 0, 0) 10px, rgba(0, 0, 0, 1) 11px);
    mask-position: 100px 350px;
  }
}
</style>
