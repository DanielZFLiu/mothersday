<template>
  <div class="content">
    <img class="background" id="background1" src="..\src\assets\油墨画1.png" alt="">
    <img class="background" id="background2" src="..\src\assets\油墨画2.png" alt="">
    <img class="background" id="background3" src="..\src\assets\油墨画3.png" alt="">
    <img class="background" id="background4" src="..\src\assets\油墨画4.png" alt="">
    <img class="background" id="background5" src="..\src\assets\油墨画5.png" alt="">
    <img class="background" id="background6" src="..\src\assets\油墨画6.png" alt="">
    <img class="background" id="background7" src="..\src\assets\油墨画7.png" alt="">
    <img class="background" id="background8" src="..\src\assets\油墨画8.png" alt="">
    <img class="background" id="boat" src="@\assets\小舟.png" alt="">
    <span class="paragraph" id="msg">{{message}}</span>
    <router-view/>
  </div>
</template>

<script>
export default{
  data(){
    return{
      message: "",
    }
  },
  methods: {

  },
  mounted() {
    // document.getElementById("boat").src = "..\\src\\assets\\小舟.png";
    setTimeout(() => {
      document.getElementById("boat").src = require('@/assets/小舟2.png');
    }, 20500);

    setTimeout(() => {
      document.getElementById("boat").src = require('@/assets/小舟3.png');
    }, 23500);

    setTimeout(() => {
      document.getElementById("boat").src = require('@/assets/小舟4.png');
    }, 26500);

    setTimeout(() => {
      document.getElementById("boat").src = require('@/assets/小舟5.png');
    }, 29000);

    setTimeout(() => {
      this.message = "";
      var msg2 = "妈，非常感谢您。接下来的就要我们尽可能单独去画了；\
但向您保证，我们会画出精彩的作品来。".split("");
      msg2.forEach((word, i) => {
        setTimeout(() => {
          this.message += word;
        }, i * 150); 
      });
    }, 30000);

    setTimeout(() => {
      this.message = "";
      document.getElementById("msg").style = "white-space: pre";
      var msg3 = "   洗衣做饭忙不完，每日忙率不着闲，\n\
   历经风霜添白发，勤劳持家不知烦，\n\
   尝尽苦辣皆为甜，养大子女无怨言。\n\
   祝福您健康长寿，愿生活中最美好\n   的幸福永远属于您。".split("");
      msg3.forEach((word, i) => {
        setTimeout(() => {
          this.message += word;
        }, i * 150); 
      });
    }, 38000);

    setTimeout(() => {
      var msg1 = "每人出生就是画手，负责画出自己或幸福或平淡或悲惨的一生。\
如果这么想的话，母亲一定就是我们画画的老师。\
以刘子枫、刘诗秋为名的画卷上，初始的部分是精细入微的画，\
洋溢着饱满又温暖的颜色。".split("");
      //forEach() always returns the value undefined,
      // and thus each "loop" will wait for the inside function to execute
      // before the next "loop"
      msg1.forEach((word, i) => {
        setTimeout(() => {
          this.message += word;
        }, i * 150); 
      });
    }, 4000);
  }
}
</script>

<style>
  .content {
    /* The CSS margin properties are used to create space around 
    elements, outside of any defined borders. 
    margin: apx bpx means that top&bottom margin is a px and
    left and right margin is b px*/
    margin: 0 auto;
    /* The max-width property defines the maximum width of an element.
    If the content is larger than the maximum width, 
    it will automatically change the height of the element. */
    /* max-width: 1200px; */
    /* Padding is used to create space around an element's content, 
    inside of any defined borders.
    padding: apx bpx means that top&bottom padding is a px and
    left and right padding is b px */
    padding: 0 20px; 

    font-family: Roboto, "Open Sans", "Helvetica Neue";
    z-index: 0;
  }

  @keyframes background1 {
    0% {opacity: 0;}
    50% {opacity: 1;}
    100% {opacity: 1;}
  }

  @keyframes background2 {
    0% {opacity: 0;}
    56% {opacity: 0;}
    62% {opacity: 1;}
    100% {opacity: 1;}
  }

  @keyframes background3 {
    0% {opacity: 0;}
    62% {opacity: 0;}
    68% {opacity: 1;}
    100% {opacity: 1;}
  }

  @keyframes background4 {
    0% {opacity: 0;}
    68% {opacity: 0;}
    74% {opacity: 1;}
    100% {opacity: 1;}
  }

  @keyframes background5 {
    0% {opacity: 0;}
    74% {opacity: 0;}
    80% {opacity: 1;}
    100% {opacity: 1;}
  }

  @keyframes background6 {
    0% {opacity: 0;}
    80% {opacity: 0;}
    86% {opacity: 1;}
    100% {opacity: 1;}
  }

  @keyframes background7 {
    0% {opacity: 0;}
    86% {opacity: 0;}
    92% {opacity: 1;}
    100% {opacity: 1;}
  }

  @keyframes background8 {
    0% {opacity: 0;}
    92% {opacity: 0;}
    98% {opacity: 1;}
    100% {opacity: 1;}
  }

  .background{
    width: 100%;
    position: fixed;
    top: auto;
    bottom: auto;
    left: 0;
  }

  #background1{
    z-index: 1;
    opacity: 0;
    animation-name: background1;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  #background2{
    z-index: 2;
    opacity: 0;
    animation-name: background2;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  #background3{
    z-index: 3;
    opacity: 0;
    animation-name: background3;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  #background4{
    z-index: 4;
    opacity: 0;
    animation-name: background4;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  #background5{
    z-index: 5;
    opacity: 0;
    animation-name: background5;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  #background6{
    z-index: 6;
    opacity: 0;
    animation-name: background6;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  #background7{
    z-index: 7;
    opacity: 0;
    animation-name: background7;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  #background8{
    z-index: 8;
    opacity: 0;
    animation-name: background8;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  @keyframes rowing {
    0% {left: -10%; opacity: 0;}
    10% {left: -10%; opacity: 1;}
    100% {left: 10%; opacity: 1;}
  }

  #boat{
    opacity: 0;
    z-index: 9;
    animation-name: rowing;
    animation-duration: 10s;
    animation-fill-mode: forwards;
    animation-delay: 18000ms;
    animation-timing-function: linear;
  }
</style>
