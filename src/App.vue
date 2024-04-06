<template>
  <div id="app">
    <van-tabs v-model="active1" style="width: 100%;">
  <van-tab title="关注">
    <van-button type="primary">主要按钮</van-button>
<van-button type="info">信息按钮</van-button>
<van-button type="default">默认按钮</van-button>
<van-button type="warning">警告按钮</van-button>
<van-button type="danger">危险按钮</van-button>
  </van-tab>
  <van-tab title="发现">内容 2</van-tab>
  <van-tab title="济南">内容 3</van-tab>
</van-tabs>

    <!-- <div class="left">
      <div @click="changState1">文字</div>
      <div @click="changeState">图片</div>
      <div>3333</div>
      <div>4444</div>
      <div>5555</div>
    </div>
    <div class="right">
      <div v-if="showWord">
        <p>1233234</p>
      <p>66666668888</p>
      <p>879788888uuu内容区域</p>
      </div>
      <img v-else src="https://tse4-mm.cn.bing.net/th/id/OIP-C.duz6S7Fvygrqd6Yj_DcXAQHaF7?w=246&h=197&c=7&r=0&o=5&dpr=2&pid=1.7" alt="">
      
    </div> -->
   <van-tabbar v-model="active">
  <van-tabbar-item >首页</van-tabbar-item>
  <van-tabbar-item >购物</van-tabbar-item>
  <van-tabbar-item ><span class="btn">+</span></van-tabbar-item>
  <van-tabbar-item >消息</van-tabbar-item>
  <van-tabbar-item >我</van-tabbar-item>
</van-tabbar>

  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      active1: 0,
       active: 0,
      // showWord: false
    }
  },
  methods: {
    // changeState() {
    //   this.showWord = false
    // },
    // changState1() {
    //   this.showWord = true
    // }

  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  /* border: 1px solid red; */
  display: flex;

  
}
.btn {
  font-size: 2rem;
  background: red;
  border-radius: 10%;
  color: #fff;
  padding: 0rem 1rem; 
}
/* .left {
  height: 358px;
    background-color: #9f8052;
    width: 221px;
    padding-top: 20px;
}
.left div {
  height: 33.6px;
    line-height: 33.6px;
    color: #fff;
    font-size: 20px;
    border-bottom: 1px dashed #fff;
  
}
.left div:hover {
  color: #f00;
  background-color: #fff;
}
.right {
  height: 358px;
    background-color: #fff;
    width: 521px;
    margin-right: 100px;
    border: 3px dashed #222;
} */
</style>
