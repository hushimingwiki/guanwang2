<template>
    <div class="box">
        <div v-for="item in productList2" :key="item._id" class="cp_introduction">
            <div class="ci_box" :style="{backgroundImage: `url(${item.image})`}">
                <div class="box">
                    
                </div>
                <!-- <div>
                    <div class="">
                        <p>{{item.name}}</p>
                    </div>
                 
                    <p style="margin-bottom: 40px;">简介：{{ item.introduction }}</p>
                    <p style="margin-bottom: 80px; line-height: 2; text-indent: 2em;">{{ item.detail }}</p>
                    <p>了解更多，请加微信：13320001761</p>
                </div> -->
            </div>
        </div>
    </div>
</template>

<script>
import { onMounted, ref } from 'vue';
import axios from 'axios';
const productList = ref([]);
export default{
    data(){
        return{
            productList2:[
                {
                    image:'/src/assets/home1.jpg',
                    name:'菜多惠',
                    introduction:'买净菜，就上菜多惠小程序。一张是净菜配送服务，方便，快捷，新鲜的菜品全在菜多惠小程序'
                }
            ]
        }
    },
    mounted() {
    console.log(this.productList2,'ppp')
    }
}

// onMounted(()=>{
//     console.log(this.productList2,'productList2')
//     // getProduct();
// })

// const getProduct = async()=>{
//     const res = await axios.get('/webapi/product/list');
//     productList.value = res.data.data;

// }

</script>

<style scoped>
.box{
    /* margin-top: 60px; */
}
.cp_introduction{
    margin: 0px;
}
.ci_box{
    width: 100%;
    height: calc(100vh);
    background-size: cover;
    background-repeat: no-repeat;
    background-position-y: -150px;
    position: relative;
    z-index: 99;
}
.item{
    width: 100%;
    height: 100%;
    background-size: cover;
}
.el-card{
    width: 50%;
    height: 100%;
    background-color: rgba(255,255,255,.7);
}

</style>