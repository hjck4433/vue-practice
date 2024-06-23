<template>
  <el-row :gutter="20">
    <el-col :span="4"
      ><div class="grid-content bg-purple-dark">col1</div></el-col
    >
    <el-col :span="4"><div class="grid-content bg-purple">col2</div></el-col>
    <el-col :span="4"
      ><div class="grid-content bg-purple-light">{{ msg }}</div></el-col
    >
    <el-col :span="4"><div class="grid-content bg-purple">col4</div></el-col>
    <el-col :span="6"><div class="grid-content bg-purple">col5</div></el-col>
  </el-row>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }
}
.el-col {
  border-radius: 4px;
  div {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
