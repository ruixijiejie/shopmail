<template>
    <div>
      <cmtbox :id="$route.params.id"></cmtbox>
    </div>
</template>

<script>
    import cmtbox from '../subcomponents/comment'
    export default {
      name: "GoodsComment",
      components: {
          cmtbox
      }
    }
</script>

<style scoped>

</style>
