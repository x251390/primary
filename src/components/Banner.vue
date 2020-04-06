<template>
  <div>
    <div class="banner">
      <div class="bannerBig">捕捉每一个美丽瞬间</div>
      <div class="bannerBox">
        <p>CAPTURE EVERY MOMENT</p>
        <p>开心-放松-美丽-自由</p>
        <p>Happy-Relax-PROOF-Beautiful-Free</p>
      </div>
    </div>
    <div class="left">
      <div>
        <p>景区中心</p>
        <p>Scenic Area Center</p>
        <ul>
          <li v-for="(item,index) in listDate" :key="index">
            <router-link :to="{path:item.to}">{{item.infor}}</router-link>
          </li>
        </ul>
        <div class="leftImg">
            <img src="../assets/u=2577925337,1742674145&fm=26&gp=0.jpg" alt="">
        </div>
        <div class="leftAdd">
            加盟热线：400-0000-0000
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      listDate: [
        {
          to: "/about",
          infor: "关于我们"
        },
        {
          to: "/about",
          infor: "关于我们"
        },
        {
          to: "/about",
          infor: "关于我们"
        },
        {
          to: "/about",
          infor: "关于我们"
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
.banner {
  padding-top: 80px;
  background: url("../assets/u=1632667888,2110156343&fm=26&gp=0.jpg");
  height: 300px;
  margin: 0 auto;
  color: #fff;
  .bannerBig {
    font-size: 38px;
    margin-bottom: 20px;
  }
  .bannerBox {
    background: url("../assets/banner_tu.png") no-repeat;
    width: 600px;
    margin: auto;
    padding: 0px 0 50px;
    & > p:nth-child(1) {
      font-size: 12px;
    }
    & > p:nth-child(2) {
      font-size: 18px;
      margin: 15px;
    }
    & > p:nth-child(3) {
      font-size: 12px;
    }
  }
}
.left {
  padding-top: 20px;
  width: 200px;
  background: blue;
  position:absolute;
  height: 500px;
  top:350px;
  margin-left: calc((100% - 1200px) / 2);
 

  p:nth-child(1) {
    color: #fff;
    font-size: 28px;
  }
  p:nth-child(2) {
    color: #fff;
    padding: 15px 0;
  }
  ul {
    list-style: none;
    background: rgb(219, 215, 215);
    li {
        border-bottom: 1px solid rgb(182, 174, 174);
        text-align: center;
        padding: 5px 0;
      a {
        text-decoration: none;
        color:#111;
      }
    }
  }
  .leftImg{
      font-size: 0;
      height: 150px;
      img{
          width: 100%;
          height: 100%;
          
      }
  }
  .leftAdd{
      padding: 15px;
      color: #fff;
      font-size: 16px;
  }
}
</style>