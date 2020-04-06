<template>
  <div class="About">
    <Banner></Banner>
    <div class="about">
      <div class="AboutCrumb">
        <el-breadcrumb separator="/">
          <el-breadcrumb-item :to="{ path: '/' }">网站首页</el-breadcrumb-item>
          <el-breadcrumb-item>
            <router-link to="/Index">关于我们</router-link>
          </el-breadcrumb-item>
        </el-breadcrumb>
      </div>
      <div class="AboutContent">
        <p>南充西山，位于四川省南充市顺庆城区西郊，主要由栖乐山、火凤山、官宝山、马鞍山、人头山、插旗山、乳泉山等12座特色山峰延绵组成。现已建成万卷楼、开汉楼、栖乐寺三大特色景区，各大景区都有其独特的自然景观和历史文化内涵，景区内树木葱郁，层林尽染，山泉潺潺，蛙鸣鸟叫；尤其是栖乐山主峰海拔480.7米，与城区绝对高差200余米，在山上俯看城区，西河在山脚缠绕，犹如白色玉带，奔嘉陵江而去，繁华都市依山而建尽收眼底，形成“山、水、城”相依的独特奇观。</p>
        <p>在城区远眺西山宛如一道绿色屏障和水墨山水画廊，将南充城区紧紧环抱在怀中，因而西山便有了果城的“绿宝石”之称，也形成了“景、城、人”相融的宜居环境。2006年被评定为国家AAAA级旅游景区后，集自然生态、三国文化、红色文化于一体的西山风景区，很快便成为了锦绣南充风物揽胜的宝地、休闲健身的乐园和“三国文化探源游”的目的地,并享有“蜀中胜景”之美誉。 西山风景区规划面积由原2006年的12.1平方公里扩大到18.8平方公里。为维持和保护“两山夹一水”的景观格局，规划形成了“一核两带、三片六区”的风景区布局。</p>
      </div>
      <div class="AboutImg">
        <el-row :gutter="24">
          <el-col :span="6">
            <div class="grid-content bg-purple">
              <img src="../assets/map.jpg" />
            </div>
          </el-col>
          <el-col :span="6">
            <div class="grid-content bg-purple">
              <img src="../assets/map.jpg" />
            </div>
          </el-col>
          <el-col :span="6">
            <div class="grid-content bg-purple">
              <img src="../assets/map.jpg" />
            </div>
          </el-col>
          <el-col :span="6">
            <div class="grid-content bg-purple">
              <img src="../assets/map.jpg" />
            </div>
          </el-col>
        </el-row>
      </div>
    </div>
  </div>
</template>
<style lang="less" scoped>
@width: calc((100% - 1200px) / 2 + 250px);
.about {
  
  margin-left: @width;
  margin-right: calc((100% - 1200px) / 2);
  width: calc(100% - (100% - 1200px) - 250px);
  .AboutCrumb {
    margin-top: 20px;
    box-sizing: border-box;
    padding: 15px;
    border: 1px solid rgb(199, 188, 188);
  }

  .AboutImg {
    box-sizing: border-box;
    padding: 15px;
    border: 1px solid rgb(199, 188, 188);
    height: 180px;
    .el-row {
      height: 100%;
      .el-col-6 {
        height: 100%;
        .grid-content {
          height: 100%;
          img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
  .AboutContent {
    margin: 20px 0;
    box-sizing: border-box;
    padding: 15px;
    border: 1px solid rgb(199, 188, 188);
    text-align: left;
    line-height: 30px;
    p:nth-child(1) {
      margin-bottom: 20px;
    }
  }
}
</style>
<script>
import Banner from "@/components/Banner";
export default {
  components: {
    Banner
  },
  data() {
    return {};
  }
};
</script>
