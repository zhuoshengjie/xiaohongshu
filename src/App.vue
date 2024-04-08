<template>
  <div id="app">
   
   <div class="pageTitle">济南租房参考</div>
   <van-search  v-model="value" placeholder="请输入搜索关键词" />
  
  <div class="list-item"  v-for="item in list" :key="item" >
   <div class="title" >{{item.title}}</div>
    <div class="content">
      
      <span >{{ item.desc }}</span>
      <span style="float: right;">{{ item.time }}</span>
    </div>
  </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
       value: '',
       list: [
          {
            title: 'XX小区避雷XX中介', 
            desc: '退房不退押金',
            time: '2020-01-01'
          },
          {
            title: '标题2',
            desc: '描述信息',
            time: '2020-01-01'
          },
          {
            title: '标题3',
            desc: '描述信息',
            time: '2020-01-01'
          }
       ],
      
      // showWord: false
    }
  },
  methods: {
    onLoad() {
      // 异步更新数据
      // setTimeout 仅做示例，真实场景中一般为 ajax 请求
      setTimeout(() => {
        for (let i = 0; i < 10; i++) {
          this.list.push(this.list.length + 1);
        }

        // 加载状态结束
        this.loading = false;

        // 数据全部加载完成
        if (this.list.length >= 40) {
          this.finished = true;
        }
      }, 1000);
    },

  },
  components: {
  }
}
</script>

<style>
#app {
  

  
}
.pageTitle {
  font-size: 24px;
  padding: 10px;
  margin-top: 10px;
  text-align: center;
}
.list-item {
  padding: 10px;
  border-bottom: 1px solid #ddd;
  .title {
    font-size: 18px;
    margin-bottom: 10px;
  }
  .content {
    font-size: 14px;
    color: #666;
  }
}
</style>
