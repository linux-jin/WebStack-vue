<template>
  <footer class="main-footer sticky footer-type-1">
    <div class="footer-inner">
      <!-- 版权信息 -->
      <div class="footer-text">
        &copy; 2017-2019
        <a
          href="https://cf-proxy.trojan.workers.dev/https/pornhub.com/"
          target="_blank"
          ><strong>NSFW</strong></a
        >
        design by
        <a href="https://github.com/beer-on-ice" target="_blank"
          ><strong>mistyhill</strong></a
        >. Do you wanna to turn on Fucking color?
        <a style="color:yellow;" href="javascript:;" @click="colorFlag"
          ><strong>{{ isOn ? 'YES' : 'NO' }}</strong></a
        >
      </div>

      <div class="go-up">
        <a href="#" rel="go-top"><i class="fa-angle-up"></i></a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      isOn: true
    }
  },
  methods: {
    colorFlag() {
      this.isOn = !this.isOn
      this.$bus.$emit('colorFlag', this.isOn)
    }
  }
}
</script>

<style></style>
