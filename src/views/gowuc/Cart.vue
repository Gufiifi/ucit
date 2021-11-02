<template>
  <div id="page-cart" class="device">
    <header>
      <router-link class="back" to="/gowuc">返回</router-link>
      <span class="header-title">购物清单</span>
      <span class="header-edit"
        ><span>编辑</span> <span style="display: none">完成</span></span
      >
    </header>
    <div class="page">
      <!-- <div class="empty-states"><span>这里是空的，快去逛逛吧</span></div> -->
      <ul class="goods-list cart-list">
        <li class="goods-item">
          <div class="item-selector">
            <div class="icon-selector">
              <svg
                t="1504061791962"
                viewBox="0 0 1024 1024"
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                p-id="2922"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                width="12"
                height="12"
                class="icon"
              >
                <path
                  d="M908.288 127.488l-537.6 537.6-254.976-254.976L0 525.824l254.976 254.976 115.712 115.712L486.4 780.8l537.6-537.6z"
                  fill="#ffffff"
                  p-id="2923"
                ></path>
              </svg>
            </div>
          </div>
          <div class="goods-img">
            <img
              src="http://img11.360buyimg.com/n1/s528x528_jfs/t3109/194/2435573156/46587/e0e867ac/57e10978N87220944.jpg!q70.jpg"
              alt="Beats EP头戴式耳机"
            />
          </div>
          <div class="goods-info">
            <p class="goods-title">Beats EP头戴式耳机</p>
            <div class="goods-price">
              <span>¥<b>558</b></span>
            </div>
            <span class="des">库存128件</span>
            <div class="goods-num">
              <div class="num-btn">+</div>
              <div class="show-num">3</div>
              <div class="num-btn">-</div>
            </div>
          </div>
        </li>
        <li class="goods-item">
          <div class="item-selector">
            <div class="icon-selector">
              <svg
                t="1504061791962"
                viewBox="0 0 1024 1024"
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                p-id="2922"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                width="12"
                height="12"
                class="icon"
              >
                <path
                  d="M908.288 127.488l-537.6 537.6-254.976-254.976L0 525.824l254.976 254.976 115.712 115.712L486.4 780.8l537.6-537.6z"
                  fill="#ffffff"
                  p-id="2923"
                ></path>
              </svg>
            </div>
          </div>
          <div class="goods-img">
            <img
              src="http://m.360buyimg.com/babel/jfs/t5197/28/400249159/97561/304ce550/58ff0dbeN88884779.jpg!q50.jpg.webp"
              alt="雀巢（Nestle）高钙成人奶粉"
            />
          </div>
          <div class="goods-info">
            <p class="goods-title">雀巢（Nestle）高钙成人奶粉</p>
            <div class="goods-price">
              <span>¥<b>60</b></span>
            </div>
            <span class="des">库存5件</span>
            <div class="goods-num">
              <div class="num-btn">+</div>
              <div class="show-num">2</div>
              <div class="num-btn">-</div>
            </div>
          </div>
        </li>
        <li class="goods-item">
          <div class="item-selector">
            <div class="icon-selector">
              <svg
                t="1504061791962"
                viewBox="0 0 1024 1024"
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                p-id="2922"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                width="12"
                height="12"
                class="icon"
              >
                <path
                  d="M908.288 127.488l-537.6 537.6-254.976-254.976L0 525.824l254.976 254.976 115.712 115.712L486.4 780.8l537.6-537.6z"
                  fill="#ffffff"
                  p-id="2923"
                ></path>
              </svg>
            </div>
          </div>
          <div class="goods-img">
            <img
              src="http://gw.alicdn.com/tps/TB19OfQRXXXXXbmXXXXL6TaGpXX_760x760q90s150.jpg_.webp"
              alt="煎炒烹炸一锅多用"
            />
          </div>
          <div class="goods-info">
            <p class="goods-title">煎炒烹炸一锅多用</p>
            <div class="goods-price">
              <span>¥<b>216</b></span>
            </div>
            <span class="des">库存2件</span>
            <div class="goods-num">
              <div class="num-btn">+</div>
              <div class="show-num">2</div>
              <div class="num-btn">-</div>
            </div>
          </div>
        </li>
      </ul>
    </div>
    <div class="action-bar">
      <div class="g-selector">
        <div class="item-selector">
          <div class="icon-selector">
            <svg
              t="1504061791962"
              viewBox="0 0 1024 1024"
              version="1.1"
              xmlns="http://www.w3.org/2000/svg"
              p-id="2922"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              width="12"
              height="12"
              class="icon"
            >
              <path
                d="M908.288 127.488l-537.6 537.6-254.976-254.976L0 525.824l254.976 254.976 115.712 115.712L486.4 780.8l537.6-537.6z"
                fill="#ffffff"
                p-id="2923"
              ></path>
            </svg>
          </div>
        </div>
        <span>全选</span>
      </div>
      <div class="action-btn buy-btn">去结算(0)</div>
      <div class="action-btn del-btn">删除(0)</div>
      <div class="total">
        合计：<span>¥<b>0</b></span>
      </div>
    </div>
  </div>
</template>
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
  border-radius: 4px;
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
}


.header-edit {
    float: right;
    padding: 0 10px;
    cursor: pointer;
}
.back{
  float: left;
}


.empty-states {
  padding-top: 60px;
  font-size: 18px;
  color: #aeb0b7;
  text-align: center;
}


.cart-list .goods-info {
  width: 68%;
}
.item-selector {
  width: 12%;
}

.icon-selector {
  position: relative;
  margin: 16px auto 0 auto;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  border: 2px solid #ccc;
  cursor: pointer;
}


.selector-active {
  background-color: #7a45e5;
  border-color: #7a45e5;
}


.selector-active .icon {
  position: absolute;
  top: 2px;
  left: 2px;
}


.goods-num {
  position: absolute;
  right: 10px;
  top: 4px;
  width: 302px;
  color: #999;
  text-align: center;
}


.show-num {
  line-height: 28px;
}


.num-btn {
  width: 100%;
  height: 24px;
  font-size: 20px;
  line-height: 20px;
  cursor: pointer;
}


.action-bar {
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 52px;
  font-size: 15px;
  background-color: #fff;
  border-top: 1px solid #ddd;
}


.g-selector {
  float: left;
  width: 70px;
  margin-left: 4%;
  height: 502px;
  cursor: pointer;
}


.g-selector .item-selector {
  position: relative;
  display: inline-block;
}


.g-selector span {
  position: absolute;
  margin-left: 20px;
  color: #5f646e;
  top: 15px;
}


.total {
  float: right;
  color: #363636;
  font-size: 14px;
  line-height: 50px;
  margin-right: 20px;
}


.total span {
  color: #7a45e5;
}


.total b {
  font-size: 17px;
  margin-left: 4px;
}


.action-btn {
  float: right;
  width: 120px;
  
  height: 100%;
  color: #fff;
  text-align: center;
  font-weight: 300;
  line-height: 52px;
  cursor: pointer;
}


.buy-btn {
  background-color: #7a45e5;
}


.del-btn {
  display: none;
  background-color: #ff4069;
}


.del-box .total {
  display: none;
}


.del-box .buy-btn {
  display: none;
}


.del-box .del-btn {
  display: block;
}




.goods-list {
    padding-top:8px;
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
    margin-top:6px;
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