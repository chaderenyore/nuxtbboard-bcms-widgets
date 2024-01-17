<template>
  <p>{{ data.blog_posts }}</p>
</template>

<script setup lang="ts">
import { BCMSEntryContentParsedItem } from '@becomes/cms-client/types';
import { PropType } from 'vue';
import { BCMSImage } from '~~/bcms-components';
import { NewBlogPostsWidget } from '~~/bcms/types';

const props = defineProps({
  data: {
    type: Object as PropType<NewBlogPostsWidget>,
    required: true,
  },
});

</script>