# erweima

1. 安装

  npm install qrcodejs2
  
2. 页面引入

  <div id="qrcode" ref="qrcode"></div>
  
  import QRCode from 'qrcodejs2'
  components: {QRCode}
  
3. 调用

  qrcode () {
    let qrcode = new QRCode('qrcode', {  
        width: 232,  // 设置宽度 
        height: 232, // 设置高度
        text: 'https://baidu.com'  //二维码链接的地址
    })  
  },
  
  this.$nextTick (function () {
    this.qrcode();
  })

  /*
    @  在需要调用的地方  这样必须这样调用  否则会出现  appendChild  null  就是id为qrcode的dom获取不到 返回结果为null
*/

