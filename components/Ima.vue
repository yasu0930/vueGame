<template>
    <div class="trump">
        <div v-for="item in 52" :key="item">
            <img :src="assetsImages[item-1]" >
        </div>
    </div>
</template>
<script>

let assetsImages = Array(52);
for (let i = 0 ;  i < 52; i++){
    assetsImages[i] = require(`~/assets/images/trump/${i+1}.gif`)
}
assetsImages.sort(function() {
  return Math.random() - Math.random();
});

export default {
  data() {
    return {
        message: 'Hello Vue.js!!',
        assetsImages 
    }
 }
//    methods: {
//     change: function(){
//     this.assetsImages = require('~/assets/images/trump/z01.gif')
//     }
//   }
}


</script>

<style>
.trump{
    cursor: pointer;
}

</style>
