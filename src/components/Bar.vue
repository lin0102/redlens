<template>
  <div class="bar-wrapper">
    <a class="btn" @click="listUpdate(1)">镜像源列表</a>
    <a class="btn" @click="listUpdate(2)">反向代理列表</a>
    <a class="btn" href="docs/">使用帮助</a>
  </div>
</template>

<script>
import { EventBus } from "../main.js";
export default {
  name: "Bar",
  methods: {
    listUpdate: choice => {
      EventBus.$emit("listUpdateMsg", choice);
    }
  }
};
</script>

<style lang="stylus" scoped>
.bar-wrapper .btn 
  font-size 16px
  margin 0 5px

</style>