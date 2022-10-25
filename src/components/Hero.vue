<script setup>
import {reactive, ref} from "vue"

const carusel = ref([
    // {
    //     id:1,
    //     img:"../assets/img/66E1647AEEFC7F4017AAF631C649F794.webp",
    //      title:"egwerfg"
    // },
    {
         id:2,
        img:require("../assets/img/images.jpeg"),
         title:"egwerfg"
    },
    {
         id:3,
        img:require("../assets/img/images1.jpeg"),
        title:"egwerfg"
    }

])

</script>


<template>  
<div>

<el-carousel indicator-position="outside">  
    <el-carousel-item v-for="(item, index) in carusel" :key="index">
        <img :src="item.img" alt="">      
        <h3>{{item.title}}</h3>
    </el-carousel-item>
  </el-carousel>
 
</div>


    
</template>


<style scoped>
.el-carousel__item h3 {
  display: flex;
  color: #475669;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>