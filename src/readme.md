
> 注：当前项目为 Serverless Devs 应用，由于应用中会存在需要初始化才可运行的变量（例如应用部署地区、函数名等等），所以**不推荐**直接 Clone 本仓库到本地进行部署或直接复制 s.yaml 使用，**强烈推荐**通过 `s init ${模版名称}` 的方法或应用中心进行初始化，详情可参考[部署 & 体验](#部署--体验) 。

# cosyvoice 帮助文档
<p align="center" class="flex justify-center">
    <a href="https://www.serverless-devs.com" class="ml-1">
    <img src="http://editor.devsapp.cn/icon?package=cosyvoice&type=packageType">
  </a>
  <a href="http://www.devsapp.cn/details.html?name=cosyvoice" class="ml-1">
    <img src="http://editor.devsapp.cn/icon?package=cosyvoice&type=packageVersion">
  </a>
  <a href="http://www.devsapp.cn/details.html?name=cosyvoice" class="ml-1">
    <img src="http://editor.devsapp.cn/icon?package=cosyvoice&type=packageDownload">
  </a>
</p>

<description>

部署知名智能语音模型CosyVoice在函数计算上

</description>

<codeUrl>



</codeUrl>
<preview>



</preview>


## 前期准备

使用该项目，您需要有开通以下服务并拥有对应权限：

<service>



| 服务/业务 |  权限  | 相关文档 |
| --- |  --- | --- |
| 函数计算 |  创建函数 | [帮助文档](https://help.aliyun.com/product/2508973.html) [计费文档](https://help.aliyun.com/document_detail/2512928.html) |

</service>

<remark>



</remark>

<disclaimers>



</disclaimers>

## 部署 & 体验

<appcenter>
   
- :fire: 通过 [Serverless 应用中心](https://fcnext.console.aliyun.com/applications/create?template=cosyvoice) ，
  [![Deploy with Severless Devs](https://img.alicdn.com/imgextra/i1/O1CN01w5RFbX1v45s8TIXPz_!!6000000006118-55-tps-95-28.svg)](https://fcnext.console.aliyun.com/applications/create?template=cosyvoice) 该应用。
   
</appcenter>
<deploy>
    
- 通过 [Serverless Devs Cli](https://www.serverless-devs.com/serverless-devs/install) 进行部署：
  - [安装 Serverless Devs Cli 开发者工具](https://www.serverless-devs.com/serverless-devs/install) ，并进行[授权信息配置](https://docs.serverless-devs.com/fc/config) ；
  - 初始化项目：`s init cosyvoice -d cosyvoice`
  - 进入项目，并进行项目部署：`cd cosyvoice && s deploy -y`
   
</deploy>

## 案例介绍

<appdetail id="flushContent">

本案例展示了如何将开源项目[CozyVoice-300M](https://modelscope.cn/studios/iic/CosyVoice-300M)部署到阿里云函数计算上,实现智能语音的合成和克隆


CozyVoice是一款出色的声音合成模型（TTS），可以3秒极速复刻声音，精控情感如笑声、呼吸声，自然语音描述即可生成高级音色。适用场景有：

+ 数字人声音克隆
+ 情感陪伴服务
+ 儿童有声读物
+ 视频娱乐

CosyVoice 目前在github已有3.9K Star ，深受广大企业和开发者喜爱

</appdetail>

## 使用流程

<usedetail id="flushContent">

### 预置语音生成

使用预置语音生成面板，您可以快速体验CozyVoice的魅力
![预置语音](https://img.alicdn.com/imgextra/i3/O1CN01tvIGqQ1y4VJMaaTox_!!6000000006525-0-tps-2880-1626.jpg)

### 定制语音生成（复刻录制声音）

注意：复刻录制声音需要通过浏览器采集您的声音，请注意安全隐私，此外，由于浏览器安全限制对于非https域名默认不会开启声音录入的能力，您使用serverless devs部署后分配的域名不会添加http证书，此时如果您想使用复刻录音的功能，请按照以下操作，增加域名的限制解除，之后按照流程复制声音
1. Chrome 开发者模式：
    ○ 您可以在 Chrome 中启用实验性标志来允许 HTTP 访问摄像头和麦克风。
步骤：

    + a. 打开 Chrome 浏览器。
    + b. 输入 chrome://flags/#unsafely-treat-insecure-origin-as-secure 并回车。
    + c. 将 Unsafely treat insecure origin as secure 设置为 Enabled。
    + d. 在 Origin to treat as secure 中输入您的 IP 地址（例如 http://127.0.0.1）。
    + e. 重启 Chrome 浏览器。
2. Firefox 开发者模式：
    ○ Firefox 也允许您在开发模式下绕过 HTTPS 限制。
步骤：

    + a. 打开 Firefox 浏览器。
    + b. 输入 about:config 并回车。
    + c. 搜索 media.getusermedia.insecure-origins.enabled。
    + d. 将此设置设置为 true。
    + e. 搜索 media.getusermedia.insecure-origins。
    + f. 添加您的 IP 地址作为值之一（例如 http://127.0.0.1）。

域名限制解除后，您可以访问 定制语音生成（复刻录制声音） 录制声音
![定制语音生成（复刻录制声音）](https://img.alicdn.com/imgextra/i4/O1CN01Znr8dp1IpU4hbid0J_!!6000000000942-0-tps-2984-1696.jpg)


### 高级语音生成（自然语言控制）
高级语音生成， 可以使用自然语言控制情感语速
![高级语音合成](https://img.alicdn.com/imgextra/i2/O1CN01RGNqNb245m6Yf9Mvu_!!6000000007340-0-tps-2812-1736.jpg)

</usedetail>

## 注意事项

<matters id="flushContent">
</matters>


<devgroup>


## 开发者社区

您如果有关于错误的反馈或者未来的期待，您可以在 [Serverless Devs repo Issues](https://github.com/serverless-devs/serverless-devs/issues) 中进行反馈和交流。如果您想要加入我们的讨论组或者了解 FC 组件的最新动态，您可以通过以下渠道进行：

<p align="center">  

| <img src="https://serverless-article-picture.oss-cn-hangzhou.aliyuncs.com/1635407298906_20211028074819117230.png" width="130px" > | <img src="https://serverless-article-picture.oss-cn-hangzhou.aliyuncs.com/1635407044136_20211028074404326599.png" width="130px" > | <img src="https://serverless-article-picture.oss-cn-hangzhou.aliyuncs.com/1635407252200_20211028074732517533.png" width="130px" > |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| <center>微信公众号：`serverless`</center>                                                                                         | <center>微信小助手：`xiaojiangwh`</center>                                                                                        | <center>钉钉交流群：`33947367`</center>                                                                                           |
</p>
</devgroup>
