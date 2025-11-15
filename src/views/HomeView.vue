<script setup>
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
      <div class="header">
        <span>Written By {{ post.author }} or {{ post.created_at }}</span>
        <div>
          <button class="del material-icons">delete</button>
          <button class="save material-icons">bookmark</button>
        </div>
      </div>
      <h1>{{ post.title }}</h1>
      <p>{{ post.body }}</p>
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

.header {
  font-size: 12px;
  background: #0284c7;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
  font-weight: 300;
  button {
    border-radius: 30px;
  }
  div .del {
    font-size: 20px;
    padding: 3px;
    background: #fff;
    color: #ef4444;
  }
  div .save {
    font-size: 20px;
    padding: 3px;
    background: #fff;
    color: #22c55e;
    margin-left: 10px;
  }
}
h1 {
  padding: 1rem;
}
p {
  padding: 0 1rem 1rem;
  font-weight: 300;
}
</style>
