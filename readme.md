| 类型 | 描述                                                         | 解决方案                                                     | 报告时间 | 版本 | 代码片段／博文 |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------- | ---- | -------------- |
| 组件 | 在组件中使用wx.createCanvasContext获取不到canvas实例         | wx.createCanvasContext('my-canvas', this)第二个参数需要加this | 0524     |      |                |
| API  | 在App中onShow生命周期中使用getApp()返回undefined             | 将getApp()改成this                                           | 0524     |      |                |
| 组件 | 使用button的open-type获取用户电话（open-type="getPhoneNumber"）或者用户信息（open-type="getUserInfo"）时，由于获取信息是异步的，用户会重复点击 | 在点击（绑定bindtap事件）按钮的时候开启loading遮罩，回调时关闭遮罩 | 0607     |      |                |
| API  | wx.showLoading和拉下刷新不能一起用，要不然会出现意想不到的结果 |                                                              | 0607     |      |                |
| 组件 | 通过用 web-view 来支持富文本不支持视频的问题                 |                                                              | 0607     |      |                |
| 组件 | 微信textarea级别非常高，定位元素设置了z-index也无法覆盖，目前还没有比较好的解决方式。 | 当失去焦点时使用view代替                                     | 0607     |      |                |
| API  | wx.switchTab: url 不支持 queryString（带参数）               | 使用全局变量传参                                             | 0619     |      |                |
| API  | 发送模版信息的时候接口报错resp:{"errcode":41030,"errmsg":"invalid page hint: [q7LoEA0699ge30]"} | 发送模版消息接口的page字段不能使用绝对地址，不能使用相对地址，使用pages/xxx/xxx而不是/pages/xxx/xxx | 0619     |      |                |
| API  | wx.request，当响应体是 json 格式，但是包含 \u2028 字符的时候，返回 data 是 String 类型，导致报错。 |                                                              | 0705     |      |                |
| 组件 | 自定义组件内，修改图标的类属性不生效                         | 在组件wxss文件中按需引入图标定义，进行修改`                  |          |      |                |
| 组件 | Android 下，Canvas 渲染的图片超过某最大值，会发生图片自动缩小问题 | 控制图片宽度不大于750rpx                                     |          |      |                |
| 组件 | image src如果是相对地址在真机显示不了                        | src要使用绝对地址                                            | 0801     |      |                |
| 组件 | 调用组件内部的方法，可以 selectComponent 获取组件示例，调用里面的方法。 |                                                              | 0802     |      |                |
| 框架 | Array.prototype.includes使用报错                             | 是由于在IOS8中不支持includes，导致报错，所以以后在写代码时要谨慎使用ES6的一些高级api | 0820     |      |                |
| API  | 使用wx.getFileSystemManager().writeFile写文件时报错fail permission denied | filePath需要使用wx.env.USER_DATA_PATH + '/xxx.js'            | 0829     |      |                |
|      |                                                              |                                                              |          |      |                |

