<template>
  <div class="about">
    <Header title='关于我们' />
    <van-divider
      content-position="left"
      :style="{ color: '#39be77', borderColor: '#39be77', padding: '0 16px' }"
    >
      关于作者
    </van-divider>
    <div class="content">
      大家好，我是小东
      <br>
      一个热爱前端的小伙子
      <br>
      很高兴认识你
      <br>
      让我们一起为前端道路添加色彩吧！！
    </div>
  </div>
</template>

<script>
import Header from '../components/Header.vue'
export default {
  name: 'About',
  components: {
    Header
  }
}
</script>

<style lang="less">
  .about {
    .content {
      padding: 0 16px;
      font-size: 14px;
      color: rgba(0, 0, 0, .5);
      line-height: 24px;
      p {
        margin-bottom: 10px;
      }
    }
  }
</style>