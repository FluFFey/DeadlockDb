<template>
  <div class ="category">
    <ShopItem/>
    <ShopItem/>
  </div>
</template>

<script>
import ShopItem from './shopitem.vue';

export default {
  data(){
    return {
    }
  },
  props: {
    compact: {
      type: Boolean,
      default: true,
    },
  },
  components:{
    ShopItem
  }
}
</script>

  <style scoped>

  /* Main card styling */
  .category {
    width: 500px;
    height: 180px;
    transition: all 0.3s ease;
    overflow: hidden;
    background-color: rgb(89,64,32);
    padding-left: 50px;
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: flex-start;
    align-items: center;
  }

  </style>