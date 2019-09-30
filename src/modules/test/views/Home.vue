<template>
    <div class="container">
        <header @click="scrollCssTest">
            <!--<img class="swiper-image" src="../assets/image/1631553082281_.pic_hd.jpg">-->
            <!--<img class="swiper-image" src="../assets/image/1631553082281_.pic_hd.jpg">-->
            <div class="area area-one"></div>
            <div class="area area-two"></div>
            <div class="area area-one"></div>
            <div class="area area-two"></div>
        </header>
        <div class="content">
            <div class="offset-test" @touchstart="handleTouchstart"></div>
        </div>
        <footer></footer>
    </div>
</template>

<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';

  @Component({
    components: {},
  })
  export default class Home extends Vue {
      private startX: number = 0;
      private currentTranslateX: number = 0;

      private scrollCssTest(e: any) {
          console.log(`e.target,`, e.target);
          console.log(`e.target.parentNode,`, e.target.parentNode);
          console.log(`e.target.parentNode.clientWidth,`, e.target.parentNode.clientWidth);
          console.log(`e.target.parentNode.scrollWidth,`, e.target.parentNode.scrollWidth);
          console.log(`e.target.parentNode.scrollLeft,`, e.target.parentNode.scrollLeft);
      }

      private handleTouchstart(e: any) {
          console.log(`handleTouchstart --------`, e);
          this.startX = e.touches[0].pageX;
          console.log(`e.target.parentNode`, e.target.parentNode);
          console.log(`e.target.offsetParent`, e.target.offsetParent);
          console.log(`e.target.offsetHeight`, e.target.offsetHeight);
          console.log(`e.target.offsetWidth`, e.target.offsetWidth);
          console.log(`e.target.offsetLeft`, e.target.offsetLeft);
          console.log(`e.target.offsetTop`, e.target.offsetTop);
          // let pageOffsetLeft = 0;
          // let curDom = e.target;
          // while (curDom.offsetParent != null) {
          //     pageOffsetLeft = curDom.offsetLeft + Number.parseInt(curDom.offsetParent.style.borderLeftWidth);
          //     curDom = curDom.offsetParent;
          // }

      }
      private handleTouchmove(e: any) {
          console.log(`handleTouchmove --------`, e);
      }
      private handleTouchend(e: any) {
          console.log(`handleTouchend --------`, e);
      }
      private handleMoveRight() {
          console.log(`handleMoveRight --------`);
      }
  }
</script>

<style lang="less" scoped>
    @import "../less/Home";
</style>