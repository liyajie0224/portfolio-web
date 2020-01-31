<template>
<!-- Make a div wrapped slider,set height and width -->
<div style="width:100%;margin: auto;height:500px">
   <!-- Using the slider component -->
   <slider ref="slider" :options="options" @slide='slide' @tap='onTap' @init='onInit'>
       <!-- slideritem wrapped package with the components you need -->
       <slideritem v-for="(item,index) in someList" :key="index" :style="item.style">
         <img :src="item.img" alt="">
       </slideritem>
       <!-- Customizable loading -->
       <div slot="loading">loading...</div>
   </slider>
</div>
</template>
<script>
// import slider components
import { slider, slideritem } from 'vue-concise-slider'
export default {
el: '#app',
data () {
   return {
     //data list [array]
     someList:[
       {
       html: 'slider1',
       style: {
         'background': '#4abf8a'
       },
       img:'../assets/banner/111.jpg'
       },
       {
         html: 'slider2',
         style: {
           background: '#4bbfc3'
         },
       img:'../assets/banner/222.jpg'

       },
       {
         html: 'slider3',
         style: {
           background: '#333'
         },
       img:'../assets/banner/333.jpg'

       }
     ],
     options: {
       effect: 'fade',
       loop: true
     }
   }
 },
 components: {
   slider,
   slideritem
 }
}
</script>