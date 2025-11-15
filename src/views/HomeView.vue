<script setup>
import PostItem from '@/components/PostItem.vue'

const posts = [
  {
    id: 1,
    title: 'This great book!',
    body: 'tellus integer feugiat scelerisque varius morbi enim nunc faucibus a pellentesque sit',
    author: 'Sarah Doe',
    created_at: '11/06/2023',
    is_saved: false,
  },
  {
    id: 2,
    title: 'Coding is fun!?',
    body: 'tellus integer feugiat scelerisque varius morbi enim nunc faucibus a pellentesque sit',
    author: 'Jon Doe',
    created_at: '06/04/2023',
    is_saved: false,
  },
  {
    id: 3,
    title: 'Vue js VS React',
    body: 'tellus integer feugiat scelerisque varius morbi enim nunc faucibus a pellentesque sit',
    author: 'Jon Doe',
    created_at: '12/30/2022',
    is_saved: false,
  },
  {
    id: 4,
    title: 'Video games',
    body: 'tellus integer feugiat scelerisque varius morbi enim nunc faucibus a pellentesque sit',
    author: 'Jon Doe',
    created_at: '05/01/2023',
    is_saved: false,
  },
]
</script>

<template>
  <div v-for="post in posts" :key="post.id">
    <div class="wrapper">
      <PostItem :post="post" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  margin: 2rem;
  background: #fff;
  box-shadow:
    rgba(0, 0, 0, 0.1) 0px 10px 15px -3px,
    rgba(0, 0, 0, 0.05) 0px 4px 6px -2px;
  margin-bottom: 2rem;
  border-radius: 1rem;
  overflow: hidden;
}
</style>
