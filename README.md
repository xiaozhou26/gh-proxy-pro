# gh-proxy-pro
## cf worker部署
打开
https://workers.cloudflare.com

注册，登陆，Start building，取一个子域名，Create a Worker。

复制 index.js 到左侧代码框，Save and deploy。如果正常，右侧应显示首页。

返回在设置中，找到环境变量，设置如下的环境变量：

GH_URLS ： 网络上公开的反代GitHub的网站

TARGET_URLS ： 网上上公开代理gh-proxy的网站

参考链接：https://github.com/hunshcn/gh-proxy/

使用fofa获取这些网站，本仓库中有我已经测试过的链接，可以使用，也可以自己来寻找。
