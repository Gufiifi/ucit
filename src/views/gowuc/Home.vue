<template>
  <div id="page-list" class="device">
    <header>
      <router-link class="cart" to="/cart">购物车</router-link>
      <span class="header-title">商品列表</span>
    </header>
    <div class="page">
      <div class="tab-wrap">
        <ul class="cate-tab">
          <!-- <li class="cate tab-active">推荐</li>
          <li class="cate">母婴</li>
          <li class="cate">鞋包饰品</li>
          <li class="cate">食品</li>
          <li class="cate">数码家电</li>
          <li class="cate">居家百货</li> -->
          <li class="cate" :class="{'tab-active':type==item.type}" v-for="item in cartType"  :key="item.id" @click="type=item.type">{{item.name}}</li>
        </ul>
      </div>
      <ul class="filter-bar">
        <li class="filter-opt price-up" :class="{'filter-active':status=='all'}" @click="status='all'">综合排序</li>
        <li class="filter-opt price-up"  :class="{'filter-active':status=='sales'}"  @click="status='sales'">销量优先</li>
        <li class="filter-opt filter-price price-up" :class="{'filter-active':status=='priceMax'||status=='priceMin'}"   @click="changePrice">价格</li>
      </ul>
      <ul class="goods-list">
         <li class="goods-item" v-for="item in showGoodsData" :key="item.id">
          <div class="goods-img">
            <img :src="item.img" alt="item.name">
            <!---->
          </div>
          <div class="goods-info">
            <p class="goods-title">{{item.name}}</p>
            <div class="goods-price">
            
              <span>¥<b>{{item.price}}</b></span>
            </div>
            <span class="des">{{item.sales}}人付款</span> <span class="save">+</span>
          </div>
        </li>
        
      </ul>
     
    </div>
  </div>
</template>
<script>
import {mapState} from "vuex"
const cartType=[
    {
        id:0,
        name:'推荐',
        type:0
    },
    {
        id:1,
        name:'母婴',
        type:1
    },
    {
        id:2,
        name:'鞋包饰品',
        type:2
    },
    {
        id:3,
        name:'食品',
        type:3
    },
    {
        id:4,
        name:'数码家电',
        type:4
    },
    {
        id:5,
        name:'居家百货',
        type:5
    },
]
let boo=true;
export default {
    data(){
        return {
            // goodsData:this.$store.state.goodsData
            cartType,
            type:0,
            status:'all'
        }
    },
    computed:{
        // goodsData(){
        //     return this.$store.state.goodsData;
        // },
        ...mapState(['goodsData']),
        showGoodsData(){
            let data=null;
            if(this.type==0){
                // return this.$store.state.goodsData;
                data=this.goodsData.map(item=>item);
            }else{
                // return  this.goodsData.filter(item=>item.type==this.type);    
                data=this.goodsData.filter(item=>item.type==this.type);
            }
            console.log(data);
            switch(this.status){
                case "all":
                    return data;
                case "sales":
                    console.log(123);
                    return data.sort((a,b)=>{
                        return b.sales-a.sales
                    });
                case "priceMax":
                    return data.sort((a,b)=>b.price-a.price);
                case "priceMin":
                    return data.sort((a,b)=>a.price-b.price);

            }
            
        }
    },
    created(){
        // console.log(this.$store);
        this.$store.dispatch('setData')
    },
    methods:{
        changePrice(){
            if(boo){
                this.status='priceMax';
                boo=false;
            }else{
                this.status='priceMin';
                boo=true;
            }
        }
    }
}
</script>
<style lang="scss" scoped>
 img{
  width: 74px;
  height: 74px;
}
.device {
    position: relative;
    float: left;
    width: 100%;
    height: 548px;
    background-color: #eee;
    // border-radius: 40px;
    overflow: hidden;
}


header {
    padding: 0 4%;
    position: relative;
    height: 44px;
    line-height: 44px;
    background-color: #fff;
    border-bottom: 1px solid #ddd;
    text-align: center;
}


.header-title {
    font-size: 16px;
    text-align: center;
}


.header-edit {
    float: right;
    padding: 0 10px;
    cursor: pointer;
}
.cart{
  float: left;
}


.tab-wrap {
    width: 100%;
    height: 60px;
    background: red;
    overflow: hidden;
}


.cate-tab {
    white-space: nowrap;
    overflow-x: scroll;
    -webkit-overflow-scrolling: touch;
    background-color: #5D4285;
}


.cate {
    display: inline-block;
    width: 80px;
    height:70px;
    color: #fff;
    line-height: 60px;
    text-align: center;
}


.tab-active {
    background-color: #9A51FF;
}


.filter-bar {
    display: flex;
    height: 40px;
    background-color: #fff;
    border-bottom: 1px solid #E5E5E5;
    line-height: 40px;
}


.filter-opt {
    position: relative;
    width: 33.3%;
    color: #5F646E;
    text-align: center;
}


.filter-active {
    // color: #7B57C5;
    color: red;
}


.filter-price:after {
    position: absolute;
    top: 13px;
    margin-left:4px;
    content: '';
    display: inline-block;
    width: 8px;
    height: 14px;
    background: url('http://ov52d8mm7.bkt.clouddn.com/arrow-default.png') no-repeat;
    background-size: 8px 14px;
}


.filter-active.price-up:after {
    background: url('http://ov52d8mm7.bkt.clouddn.com/arrow-down.png') no-repeat;
    background-size: 8px 14px;
}


.filter-active.price-down:after {
    background: url('http://ov52d8mm7.bkt.clouddn.com/arrow-up.png') no-repeat;
     background-size: 8px 14px;
}


.goods-list {
    padding-top: 8px;
    height: 513px;
    overflow-y: scroll;
}


.cart-list {
    height: 560px;
}


.goods-item {
    display: flex;
    margin-bottom: 8px;
    padding: 10px 6px;
    min-height: 62px;
    background: #fff;
    width: 100%;
    box-sizing: border-box;
}


.goods-img {
    position: relative;
    margin-right: 4%;
    display: block;
    width: 16%;
}


.goods-img img {
    position: absolute;
    top: 0;
    left: 0;
}


.goods-item .flag {
    position: absolute;
    top: 0;
    left: 0;
    width: 20px;
    height: 20px;
    font-size: 12px;
    color: #fff;
    text-align: center;
    line-height: 20px;
    background-color: #FC5951;
    border-radius: 50%;
}


.goods-info {
    position: relative;
    width: 80%;
    text-align: left;
}


.goods-title {
    width: 80%;
    height: 38px;
    color: #363636;
    line-height: 1.4;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
}


.goods-price {
    margin-top: 6px;
    line-height: 1;
}


.goods-price span {
    font-size: 15px;
    color: #7a45e5;
    /*   background: linear-gradient(90deg, #03D2B3 0, #2181FB 80%, #2181FB 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent; */
}


.des {
    font-size: 12px;
    color: #888;
}


.save {
    position: absolute;
    right: 10px;
    bottom: 2px;
    width: 32px;
    height: 22px;
    background-color: #7a45e5;
    font-size: 16px;
    line-height: 19px;
    text-align: center;
    color: #fff;
    border-radius: 12px;
    overflow: hidden;
}


</style>