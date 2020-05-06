<template>
  <section>
    <h2>我是:{{ userName }}</h2>
  </section>
</template>

<script>
import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
  onErrorCaptured,
  onRenderTracked,
  onRenderTriggered
} from "vue";
export default {
  name: "User",
  props: {
    userName: String
  },
  setup(props, context) {
    console.log("setup 组件入口函数");
    // context.attrs
    // context.slots
    // context.parent
    // context.root
    // context.emit
    // context.refs
    console.log(`组件传递props${props.userName}`);
    console.log(`组件的上下文对象${context}`);

    onRenderTracked(() => {
      console.log("onRenderTracked");
    });
    onRenderTriggered(event => {
      console.log("onRenderTriggered");
    });
    onBeforeMount(() => {
      console.log("onBeforeMount");
    });
    onMounted(() => {
      console.log("onMounted");
    });
    onBeforeUpdate(() => {
      console.log("onBeforeUpdate");
    });
    onUpdated(() => {
      console.log("onUpdated");
    });
    onBeforeUnmount(() => {
      console.log("beforeDestroy");
    });
    onUnmounted(() => {
      console.log("onUnmounted");
    });
    onErrorCaptured(() => {
      console.log("onErrorCaptured");
    });
    return {};
  }
};
</script>