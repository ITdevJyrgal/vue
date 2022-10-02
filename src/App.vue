<template>
  <div>
    <div>
      <button v-on:click="addLike">like</button>
      <button v-on:click="addDisLike">dislike</button>
    </div>

    <div>like: <strong>{{ likes }} </strong></div>
    <div>dis like: <strong>{{ disLikes }} </strong></div>
    <div class="btn">
      <button>click</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      likes: 0,
      disLikes: 5
    }
  },
  methods: {
    addLike() {
      this.likes += 1;
    },
    addDisLike() {
      this.disLikes -= 1;
    }
  }
}
</script>

<style scoped>
.btn {
  display: flex;
  justify-content: center;
  align-items: center;
}

.btn button {
  padding: 10px 30px ;
  background: red;
  border-radius: 20px;
}
</style>