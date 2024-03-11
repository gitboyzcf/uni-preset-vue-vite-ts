<template>
  <view class="content">
    <image class="logo" src="/static/logo.png" />
    <view class="text-area">
      <text class="title">{{ countStore.count }}</text>
      <button @click="countStore.increment"></button>
    </view>
  </view>
</template>

<script setup lang="ts">
import { useCountStore } from '@/store/count'

const countStore = useCountStore()
console.log(123)
</script>

<style scoped lang="scss">
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  .logo {
    width: 200rpx;
    height: 200rpx;
    margin: 200rpx auto 50rpx;
  }
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
