<template>
  <header></header>
</template>

<script>
export default {
  name: 'main',
  props: {
    msg: String,
  },
};
</script>

<style scoped>
header {
  background-color: #def;
  min-height: 50px;
  border-bottom: solid 1px #aaa;
}
</style>
