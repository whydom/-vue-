<template>
<!-- 和 vue-router3 一样，展示路由的组件的地方 -->
  <router-view />
  <!-- 是否隐藏下面导航栏 -->
  <NavBar v-if="show" />
</template>

<script>
// 引入导航栏的组件
import NavBar from './components/NavBar.vue';
// 引入路由
import { useRouter } from 'vue-router'
import { reactive, toRefs } from 'vue'
export default {
  name: 'App',
  components: {
    NavBar
  },
  setup() {
    const state = reactive({
      menu: ['/user', '/home', '/data'],
      show: false
    })
    // 创建路由的实例对象
    const router = useRouter()
    router.afterEach(() => {
      // menu 内的路径都是需要展示底部导航栏的
      state.show = state.menu.includes(router.currentRoute.value.path)
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>
