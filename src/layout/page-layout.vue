<template>
  <router-view v-slot="{ Component, route }">
    <transition name="fade" mode="out-in" appear>
      <component
        :is="Component"
        v-if="route.meta.ignoreCache"
        :key="route.fullPath"
      />

    </transition>
  </router-view>
  主页
</template>

<script lang="ts" setup>
</script>

<style scoped lang="less"></style>
