<template>
  <div>
    <slot />
  </div>
</template>

<script setup lang="ts">
import { BCMSImageConfig } from '@becomes/cms-most/frontend';

BCMSImageConfig.cmsOrigin = 'http://localhost:8080';
BCMSImageConfig.publicApiKeyId = '65a519add71299bddf4211d1';
BCMSImageConfig.localeImageProcessing = true;
</script>
