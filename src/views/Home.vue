<template>
  <div id="Home">
    <div class="header clearfix container">
      <div class="left">你好，欢迎您访问南充官方网站1111</div>
      <div class="right">
        <span class="headerSet">设为首页</span>
        <span class="headerAdd">加入收藏</span>
      </div>
    </div>
    <!-- 搜索 -->
    <div class="search clearfix container">
      <div>
        <router-link to="/about">
          <img class="logo" src="@/assets/logo (2).png" alt="这是logo" />
        </router-link>
        <span class="logoFont">南充西山官方网站</span>
      </div>
      <div>
        <input type="text" placeholder="请输入关键字" />
        <button>搜索</button>
      </div>
      <div class="tel">
        <span>24小时在线</span>
        <span>400-0000-0000</span>
      </div>
    </div>
    <div class="list">
      <el-tabs class :tab-position="tabPosition" style="height: 200px;">
        <el-tab-pane label="网站首页">
          <Index></Index>
        </el-tab-pane>
        <el-tab-pane label="关于我们">
          <About></About>
        </el-tab-pane>
        <el-tab-pane label="景区概况">景区概况</el-tab-pane>
        <el-tab-pane label="活动盛事">活动盛事</el-tab-pane>
        <el-tab-pane label="景区攻略">景区攻略</el-tab-pane>
        <el-tab-pane label="在线留言">在线留言</el-tab-pane>
        <el-tab-pane label="联系我们">联系我们</el-tab-pane>
      </el-tabs>
    </div>
  </div>
</template>

<script>
import Index from "./Index";
import About from "./About"
export default {
  components:{
    Index,
    About
  },
  data() {
    return {
      tabPosition: "top"
    };
  }
};
</script>

<style lang="less" scoped>
.container {
  padding-left: calc((100% - 1200px) / 2);
  padding-right: calc((100% - 1200px) / 2);
  margin: 0 auto;
}
.clearfix {
  overflow: hidden;
}
.left {
  float: left;
}
.right {
  float: right;
}
@le30: {
  margin-left: 30px;
};

#Home {
  .header {
    padding-top: 10px;
    padding-bottom: 10px;
    font-size: 12px;
    color: rgb(141, 143, 136);
    border-bottom: 1px solid rgb(170, 152, 152);

    .headerAdd,
    .headerSet {
      @le30();
    }
  }
  .search {
    margin: 20px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .tel {
      span {
        display: block;
      }
      span:nth-child(1) {
        font-size: 12px;
      }
      span:nth-child(2) {
        font-size: 24px;
      }
    }
    input {
      border: 1px solid pink;
      padding: 5px;
    }
    button {
      padding: 5px 12px;
      border-left: none;
      position: relative;
      top: 1px;
      background: pink;
      border: none;
    }
    .logo {
      height: 40px;
      width: 40px;
    }
    .logoFont {
      position: relative;
      top: -10px;
      left: 5px;
    }
  }
  .list {
     /deep/.el-tabs__header{
        margin-bottom: 0!important;
        .el-tabs__nav-wrap::after{
          height: 0!important;
        }
         /deep/.el-tabs__nav-wrap {
      background: blue !important;

      color: #fff !important;
      padding: 5px;
      text-decoration: none;
      padding-left: calc((100% - 1200px) / 2);
      padding-right: calc((100% - 1200px) / 2);
      margin: 0 auto;
      /deep/.el-tabs__active-bar {
        height: 0 !important;
      }
     
     
      
      /deep/ .el-tabs__item.is-active {
        color: #fff !important;
      }
      .el-tabs__item {
        color: #fff !important;
        width: calc(1200px / 7);
      }
    }
      }
   
  }
}
</style>
