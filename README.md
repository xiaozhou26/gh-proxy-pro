# gh-proxy-pro

## 项目优点：几乎不使用woker的流量，woker仅仅做重定向的工作，极小减轻了本地或者woker的压力

## 在 Cloudflare Workers 上部署 GH-Proxy-Pro 的指南


### 第一步：注册 Cloudflare Workers

首先，打开 Cloudflare Workers 官网（[https://workers.cloudflare.com](https://workers.cloudflare.com)），如果你还没有账户，需要进行注册。完成注册并登录后，点击“Start building”按钮开始你的项目。

### 第二步：创建 Worker 和选择子域名

系统会引导你选择一个子域名，这将是你的 Worker 访问地址的一部分。选择一个对你来说意义重大且易于记忆的名称。完成后，点击“Create a Worker”进入编程界面。

### 第三步：部署代码

在这一步，你将需要 `index.js` 的代码。这段代码是 GH-Proxy 服务的核心，负责处理所有的请求和转发。你可以在 GH-Proxy 的官方 GitHub 仓库中找到这段代码（参考链接：[https://github.com/hunshcn/gh-proxy/](https://github.com/hunshcn/gh-proxy/)）。

将 `index.js` 的内容复制到 Cloudflare Workers 编辑器的左侧代码框中。检查无误后，点击“Save and Deploy”。如果一切顺利，你将在右侧预览窗口看到服务的首页。

### 第四步：配置环境变量

为了让你的 GH-Proxy 服务正常运行，你需要设置一些环境变量。回到你的 Worker 设置页面，寻找环境变量设置部分，并添加以下两个环境变量：

- `GH_URLS`：这个变量应该包含一系列网络上公开的、可以用来反代 GitHub 的网站地址。
- `TARGET_URLS`：这个变量则应包括一些网上公开的、部署 GH-Proxy 服务的网站地址。

你可以使用 FOFA 或其他网络搜索工具来获取这些地址。此外，GH-Proxy 官方仓库中也提供了一些已经测试过的链接，你可以直接使用或者自行寻找合适的资源。

### 结语

通过以上步骤，你应该已经成功部署了自己的 GH-Proxy 服务。
