<template>
  <div>
    <el-select v-model="value" placeholder="Select">
      <el-option
        v-for="item in options"
        :key="item.value"
        :label="item.label"
        :value="item.value"
      >
      </el-option>
    </el-select>
    <div>currVal : {{ value }}</div>
    <div>prevVal : {{ prevVal }}</div>
  </div>
</template>
<script>
export default {
  name: "SelectComp",
  props: {
    options: {
      type: Array,
      required: true,
      validator(value) {
        return value.every((option) => {
          return (
            typeof option.value === "string" && typeof option.label === "string"
          );
        });
      },
    },
  },
  data() {
    return {
      value: "",
      prevVal: "",
    };
  },
  computed: {
    isValueChg: function () {
      return console.log("valueChg ! : " + this.value);
    },
  },
  watch: {
    value: function (newVal, oldVal) {
      this.prevVal = oldVal;
    },
  },
};
</script>
