# 如何在本地进行微信开放平台开发调试测与试

在进行开放平台开发时，最担心的事情就是调试。当应用出问题时，能否有测试或者调试环境进行问题查找以及修复成为解决问题的关键，当然如果在开发阶段以及上线后一直有一个在本地能测试调试的环境，对开发者来说是莫大的欢喜。这次就和大家来分享一下，如何在本地对微信开发平台接入时进行实时调试和测试。

## 步骤如下（4个步骤）

1. 首先你需要申请一个公众账号作为测试账号（因为你总不能把正式推广的账号作为测试账号）
2. 在微信公众管理后台配置好测试账号的服务器测试地址
3. 在域名服务商那边进行DNS域名配置，将测试域名指向自己（公司）内网出口ip。
  + 下图为设置界面（安全宝）
  + ![DNS域名配置](https://mmbiz.qlogo.cn/mmbiz/E7ia3F4UicMx8k28bBHO9FMYsNxicX7BGB5DgaEEhIapvUOW7hSXNGWP4t6uoeHicdL7C9iaMaHuFx0hHMQHQt2uctA/0?wx_fmt=png)
4. 在自己（公司）内网的路由器进行端口映射，将内网的某个端口指向开发者本机的ip以及端口
  + 下图为设置界面（tp-link）
  + ![路由器进行端口映射](https://mmbiz.qlogo.cn/mmbiz/E7ia3F4UicMx8k28bBHO9FMYsNxicX7BGB5gQ6aEYEA7Pbt1keADa3LE93ePHjSvCkKwdRrx6qic8uxvN3MxpxTIpw/0?wx_fmt=png)
  + 对上图解释：笔者的内网ip为192.168.1.120，将路由器的8006端口指向笔者机器的8006端口。

*注意，内网ip和内网出口ip的区别:内网ip在这里是指自己（公司）某一台局域网的机器ip,内网出口ip(网络提供商给定)是指外部网络访问内网的ip*

以上四个步骤都弄好之后，就能愉快地在本地8006端口对微信开放平台开发进行调试了。
