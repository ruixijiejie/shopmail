<template>
  <div class="mui-numbox" data-numbox-min='1'>
    <button class="mui-btn mui-btn-numbox-minus" type="button">-</button>
    <input id="test" class="mui-input-numbox" type="number" value="1" @change="countChanged" ref="numbox"/>
    <button class="mui-btn mui-btn-numbox-plus" type="button">+</button>
  </div>
</template>

<script>
    export default {
      name: "goodsinfo-numbox",
      methods: {
        countChanged() {

          this.$emit("getcount", parseInt(this.$refs.numbox.value));
        }
      },
      props: ["max"],
      watch: {
        max: function (newVal,oldVal) {
          this.mui('.mui-numbox').numbox().setOption("max", newVal)
        }
      },
      mounted() {
        this.mui('.mui-numbox').numbox()
      }
    }
</script>

<style lang="scss" scoped>

</style>
