<template>
    <ul>
      <li v-for="post in posts" :key="post.title">
        <p>{{ post.title }}</p>
      </li>
    </ul>
</template>

<script lang="ts" setup>

const { data: posts } = await useAsyncData('blog', () => queryContent('/blog').find())

</script>