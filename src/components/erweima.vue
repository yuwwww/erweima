<template>
  <div
    id="qrcode"
    ref="qrcode"
  ></div>
</template>

<script>
import QRCode from "qrcodejs2"; // 引入qrcode
export default {
  name: "qrcode",
  components: { QRCode },
  methods: {
    qrcode() {
      let qrcode = new QRCode("qrcode", {
        width: 100, // 设置宽度
        height: 100, // 设置高度
        text:
          "https://ips.netnotary.cn/attestation/O6VNJIGE8Z8TBKE8H417A4IWX4KNBGSK"
      });
    }
  },

  mounted() {
    this.$nextTick(function() {
      this.qrcode();
    });
  }
};
</script>

<style scoped>
</style>