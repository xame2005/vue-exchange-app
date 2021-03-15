<template>
  <div>
    <px-assets-table v-bind:assets="assets" />
  </div>
</template>

<script>
import API from "@/api";
import PxAssetsTable from "@/components/PxAssetsTable";

export default {
  name: "Home",

  components: { PxAssetsTable },

  data() {
    return {
      assets: []
    };
  },

  created() {
    API.getAssets().then(assets => (this.assets = assets));
  }
};
</script>

<style lang="scss" scoped></style>
