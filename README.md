# ChannelFlow 客户端

免 Docker 的本机监听、转发与 HipoBuy 客户端。用户电脑无需安装 Docker、WSL、Python、Git 或 FFmpeg；HipoBuy 的引擎和浏览器仅在需要时下载。

## 下载 v0.2.2 预览版

| 系统 | 下载 |
| --- | --- |
| Windows 10/11 x64 | [Windows 客户端](https://github.com/0xliangjiang/channelflow-software/releases/download/v0.2.2/ChannelFlow-0.2.2-windows-amd64.zip) |
| macOS Apple Silicon（M 系列） | [Mac ARM64 命令行包](https://github.com/0xliangjiang/channelflow-software/releases/download/v0.2.2/ChannelFlow-0.2.2-darwin-arm64.tar.gz) |
| macOS Intel | [Mac x64 命令行包](https://github.com/0xliangjiang/channelflow-software/releases/download/v0.2.2/ChannelFlow-0.2.2-darwin-x86_64.tar.gz) |

[全部版本与附件](https://github.com/0xliangjiang/channelflow-software/releases) · [使用说明](使用说明.md) · [SHA-256 校验](SHA256SUMS.txt)

## 开始使用

Windows：解压整个文件夹，保留 `_internal`，双击 **ChannelFlow.exe**。在网页创建私有节点，将平台地址、节点 ID 和首次注册令牌填入客户端，点击“连接并启动”。窗口可留在托盘运行，退出会停止本机任务。

macOS：解压后进入 ChannelFlow 文件夹，在终端运行：

```sh
./channelflow connect --control-url https://channelflow.cc --node-id 网页上的节点ID
./channelflow start
./channelflow status
```

注册令牌按提示隐藏输入，账号和规则仍在网页配置。首次运行如提示无法验证开发者，请在确认来源和校验值后按 [Apple 官方说明](https://support.apple.com/zh-cn/102445)确认打开。

## 在同一个客户端启用 HipoBuy

Windows：点击 **安装 / 启用 HipoBuy**，等待引擎与浏览器下载、校验完成；客户端取得网页授权后，点击 **打开 HipoBuy 工作台**。本机登录码可复制，五分钟内一次有效。

macOS：

```sh
./channelflow hipobuy install
./channelflow hipobuy status
./channelflow hipobuy open
```

HipoBuy 需要原有账号和订阅授权。API Key 在本机工作台填写，图库、索引、密钥和待处理任务留在自己电脑。可用 `hipobuy disable` 暂停、`hipobuy enable` 恢复；保留全部数据。退出客户端或电脑关机、休眠、断网会影响本机任务，不会自动切换云端。

原 Docker 安装与工作台继续保留。不要让旧 Docker 和新客户端同时运行同一个来源账号；旧节点、队列与数据不自动迁移。需要迁移来源时，使用网页的显式迁移流程并确认旧来源已停止。

## 更新与验证

从旧版更新：先停止客户端，替换完整程序文件夹，再启动。保留 Windows `%LOCALAPPDATA%\ChannelFlow` 或 macOS `~/Library/Application Support/ChannelFlow` 数据目录，无需重新注册原节点。

支持 Discord、Telegram、飞书和 X 普通转发，并可选安装 HipoBuy。QQ、Discord/Telegram AI 专用进程暂未包含。已在 Windows x64、macOS Apple Silicon 和 Intel 构建并运行打包程序，验证浏览器、本机登录、节点授权、加密保存和重启恢复。真实平台账号连接、识图效果及 Discord 目标回复仍需实际验收。安装包尚未配置开发者签名或 Apple 公证。

本仓库仅分发安装包、说明和校验文件；下载软件不替代平台的账号、订阅和节点授权。

客户端 v0.2.2 内置 HTTPS 根证书；HipoBuy 组件保持 v0.2.0，由客户端自动下载，更新基础程序无需重新下载组件。
