<template>
  <div class="container">
    <h2>推荐书单</h2>
    <div class="shell">
      <div class="box">
        <a href="https://www.ituring.com.cn/book/2472">
          <div class="images">
            <img src="./images/1.jpg" />
          </div>
          <div class="content">
            <!-- <h2>123</h2> -->
            <p>JavaScript“红宝书” 前端圈公认的经典</p>
          </div>
        </a>
      </div>
      <div class="box">
        <a href="https://www.ituring.com.cn/book/2675">
          <div class="images">
            <img src="./images/2.jpg" />
          </div>
          <div class="content">
            <!-- <h2>123</h2> -->
            <p>深入讲解Vue.js实现原理和思想</p>
          </div>
        </a>
      </div>
      <div class="box">
        <a href="https://www.ituring.com.cn/book/1272">
          <div class="images">
            <img src="@/assets/images/3.jpg" />
          </div>
          <div class="content">
            <!-- <h2>123</h2> -->
            <p>国内唯一一本介绍Three.js的技术书</p>
          </div>
        </a>
      </div>
      <div class="box">
        <a href="https://www.ituring.com.cn/book/1290">
          <div class="images">
            <img src="./images/4.jpg" />
          </div>
          <div class="content">
            <!-- <h2>123</h2> -->
            <p>第一本深度讲解Node的图书</p>
          </div>
        </a>
      </div>
      <div class="box">
        <a href="https://www.ituring.com.cn/book/2882">
          <div class="images">
            <img src="./images/5.jpg" />
          </div>
          <div class="content">
            <!-- <h2>123</h2> -->
            <p>放下大部头，换一种方式入门编译原理</p>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardList",
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
h2 {
  height: 20px;
  line-height: 55px;
  color: rgb(77, 77, 77);
}
.container {
  margin-top: 2vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  justify-items: center;
  width: 90vw;
  min-width: 90vw;
  background-color: rgb(244 244 242);
}
.shell {
  position: relative;
  min-width: 1000px;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  align-content: flex-start;
  /* 3d变化 */
  transform-style: preserve-3d;
  /* 透视效果 */
  perspective: 900px;
}
.shell .box {
  position: relative;
  width: 200px;
  height: 250px;
  transition: 0.3s;
  overflow: hidden;
  margin: 30px;
  transform: rotateY(0);
  transition-delay: 0.1s;
  border-radius: 5px;
  border: #fff 5px solid;
}
.shell .box .images img {
  width: 100%;
  height: 100%;
}
.shell:hover .box {
  transform: rotateY(20deg);
}
.shell .box:hover {
  transform: rotateY(0deg) scale(1.25);
  box-shadow: 0 25px 40px rgba(0, 0, 0, 0.7);
  z-index: 1;
}
.shell .box:hover ~ .box {
  transform: rotateY(-20deg);
}
.shell .box .content {
  position: absolute;
  top: 0;
  width: 90%;
  height: 100%;
  z-index: 999;
  padding: 15px;
}

.shell .box .content p {
  color: #000;
  transition: 0.3s;
  font-size: 14px;
  transform: translateY(600px);
  background-color: rgba(255, 255, 255, 0.7);
  text-align: center;
}
.shell .box:hover .content p {
  transform: translateY(195px);
}
</style>