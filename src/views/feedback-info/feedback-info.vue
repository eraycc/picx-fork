<template>
  <div class="page-container feedback-page-container">
    <div class="help-info-item description">🏞️ {{ $t('feedback.text_1') }}</div>

    <div class="help-info-item">
      🌍 {{ $t('feedback.text_2') }} {{ $t('shortcut_key') }}：<code>{{ shortcutKey }}</code>
    </div>
    
    <div class="help-info-item">
      ❤ 博客：
      <el-link type="primary" href="https://blog.eray.cc/" target="_blank">忆光博客</el-link>
    </div>
    
    <div class="help-info-item red-text">
      <strong> ⚠️ {{ $t('feedback.text_4') }} </strong>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { getOSName } from '@/utils'

const shortcutKey = computed(() => (getOSName() === 'win' ? 'Ctrl + D' : 'Command + D'))
</script>

<style scoped lang="stylus">
@import "./feedback-info.styl"
</style>
