### 微信小程序二维码生成

page 页面写canvas
```html
<canvas id="myCanvas" style="width: 200px; height: 200px;" ></canvas>
```
调用方式
```js
// 导入
const {QR} = require('qrcode')
// 调用
QR.drawQrcode(config)
// 示例
 QR.drawQrcode({
  width: 200,
  height: 200,
  canvasId: 'myCanvas',
  text: 'https://www.baidu.com',
  image: {
    src: '',
    dWidth: 0,
    dHeight: 0
  }
})

```

### 参数 config
参数| 说明 | 示例 |
---| ----- | ----| 
width|必须，宽度 | 200 |
height|必须，高度| 200 |
canvasId|必须，id| 200 |
text|必须，内容| 200 |
x|非必须，水平位置| 0 |
y|非必须，垂直位置| 0 |
correctLevel|非必须，二维码纠错级别| 1 |
background|非必须，背景色| #fff |
foreground|非必须，前景色| #000 |
ctx|非必须，canvas上下文| wx.createCanvasContext(canvasId) |
_this|非必须，page this|  |
image|非必须，图片| {} |

### image 

参数| 说明 | 示例 |
---| ----- | ----| 
dwidth|非必须，宽度 | 50 |
dheight|非必须，高度| 50 |
src|非必须，图片路径|  |