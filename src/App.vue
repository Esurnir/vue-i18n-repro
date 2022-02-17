<script setup lang="ts">
import { computed } from "vue";
import { useI18n } from 'vue-i18n'

const { t } = useI18n();
const defaultReturn = computed(() => t('defaultReturn'));
const messageTranslated = computed(() => t('message', defaultReturn.value));
const messageFallback = computed(() => t('onlyEnglish', defaultReturn.value));
const messageDefault = computed(() => t('jfoiajeo', defaultReturn.value));

</script>

<template>
  <p>Message with all translation : {{ messageTranslated }}</p>
  <p>Message with fallback : {{ messageFallback }}</p>
  <p>Message with default : {{ messageDefault }}</p>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
