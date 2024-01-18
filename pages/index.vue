<template>
  <h1>Hello world</h1>
  
  <ClientOnly>
    <ContentManager :item="homepageData?.content.en" v-if="homepageData" />
  </ClientOnly>
</template>


<script lang="ts" setup>
import { HomePageEntry } from '~~/bcms/types';

const { data } = useAsyncData(async (ctx) => {
  const homepage = (await ctx?.$bcms.entry.get({
    template: '65a1a3b2a07a1732302f8db5',
    entry: "home"
  })) as HomePageEntry;
  return { homepage }
});

const homepageData = data.value?.homepage;
</script>

<style></style>
