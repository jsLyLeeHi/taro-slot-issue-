<template>
  <view>
    <text>{{ msg }}</text>
    <!-- 插槽无法使用-taro 3.2.0也试了 同样的问题 -->
    <Test>{{ msg }}</Test>
  </view>
</template>

<script>
import { ref } from "vue";
import Test from "./test.vue";
import "./index.less";

export default {
  components: {
    Test,
  },
  setup() {
    const msg = ref("Hello world");
    return {
      msg,
    };
  },
};
</script>
