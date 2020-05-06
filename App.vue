<template>
  <section>
    <h2>{{ title }}</h2>
    <User :userName="'虎克小哥哥'"></User>
    <h3>我是：{{userInfo.userName}}</h3>
  </section>
</template>

<script>
// @ is an alias to /src
import User from "./components/User.vue";
import { reactive, ref } from "vue";

export default {
  // setup() 函数是 vue3 中统一的入口函数,所有生命周期函数定义都是需要定义在次函数下才生效，
  // setup 函数中无法访问到 this，所有的组件参数都是通过，setup函数中包含props和context参数，props参数默认是响应式的
  setup() {
    const userInfo = reactive({ userName: "虎克小哥哥" });

    return {
      title: "Hello World Vue3.0",
      userInfo
    };
  },
  components: {
    User
  }
};
</script>

<style>
body {
  padding: 50px;
  color: #42b983;
  text-align: center;
  background-color: #282c34;
}
</style>
