<template>
  <div class="home-recommend">
    <div v-for="item in recommend" class="home-recommend-item" :key="item.sort">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>

  export default {
    name: "HomeRecommendView",
    props: {
      recommend: {
        type: Array,
        default() {
          return []
        }
      }
    }
  }
</script>

<style scoped>
  .home-recommend {
    display: flex;
    text-align: center;
    width: 100%;

    margin: 10px 0;
    padding: 0 0 10px;
    border-bottom: 10px solid #eee;
  }

  .home-recommend-item{
    flex: 1;
    width: 25%;
  }

  .home-recommend-item img{
    width: 80%;
    margin-bottom: 10px;
  }
</style>
