<template>
  <component :is="Icon" v-for="(Icon, key) in icons" :key="key" class="icon" />
  <hr />
  <component
    :is="`BvIcon${key}`"
    v-for="key in Object.keys(icons)"
    :key="key"
    class="icon"
  />
</template>

<script lang="ts" setup>
import { icons } from '@bootstrap-vue-plus/icons-vue/global'
</script>

<style>
.icon {
  height: 48px;
  color: #409eff;
}
</style>
