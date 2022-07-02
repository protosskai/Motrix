<template>
  <el-container class="content panel" direction="vertical">
    <el-header class="panel-header" height="84">
      <h4 class="hidden-xs-only">{{ title }}</h4>
    </el-header>
  </el-container>
</template>

<script>
export default {
  name: "mo-mikan-search",
  data() {
    return {};
  },
  computed: {
    title() {
      return this.$t("mikan.bangumi-search");
    }
  }
};
</script>
