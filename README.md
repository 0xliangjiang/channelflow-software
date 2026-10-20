# ChannelFlow 客户端

免 Docker 的本机监听与转发客户端。用户电脑无需安装 Python、Git 或 FFmpeg。

## 下载 v0.1.0 预览版

| 系统 | 下载 | 大小 |
| --- | --- | --- |
| Windows 10/11 x64 | [Windows 安装包](https://github.com/0xliangjiang/channelflow-software/releases/download/v0.1.0/ChannelFlow-0.1.0-windows-amd64.zip) | 133 MiB |
| macOS Apple Silicon（M 系列） | [Mac ARM64 命令行包](https://github.com/0xliangjiang/channelflow-software/releases/download/v0.1.0/ChannelFlow-0.1.0-darwin-arm64.tar.gz) | 59 MiB |
| macOS Intel | [Mac x64 命令行包](https://github.com/0xliangjiang/channelflow-software/releases/download/v0.1.0/ChannelFlow-0.1.0-darwin-x86_64.tar.gz) | 64 MiB |

[全部版本与附件](https://github.com/0xliangjiang/channelflow-software/releases) · [使用说明](使用说明.md) · [SHA-256 校验](SHA256SUMS.txt)

## 开始使用

Windows：解压整个文件夹，双击 **ChannelFlow.exe**。请保留旁边的 `_internal` 目录。在网页创建私有节点后，将平台地址、节点 ID 和首次注册令牌填入客户端，点击“连接并启动”。关闭窗口进入托盘；托盘菜单可退出并停止任务。

macOS：解压后进入 ChannelFlow 文件夹，在终端运行：

```sh
./channelflow connect --control-url https://channelflow.cc --node-id 网页上的节点ID
./channelflow start
./channelflow status
```

注册令牌按提示隐藏输入。规则、账号和目标仍在网页配置。

首次运行若出现“无法验证开发者”提示，在确认来源和校验值后，可前往 **系统设置 → 隐私与安全性 → 仍要打开**，再确认“打开”。请参考 [Apple 官方说明](https://support.apple.com/zh-cn/102445)。

## 当前范围

支持 Discord 普通账号、Telegram 用户账号、飞书用户账号和 X 数据源。QQ 托管客户端、Discord/Telegram AI 专用进程及 HipoBuy 引擎暂未包含。电脑关机、休眠或断网会影响本机任务。登录自启动仅在用户登录后生效。

本版通过 616 项本地 worker 回归及 Windows x64、macOS ARM64、macOS Intel 打包运行检查。真实平台账号登录和目标收件仍需实际验收。未配置开发者签名或 Apple 公证。

本仓库仅用于分发安装包、说明和校验文件。安装包的下载权限不替代平台的账号、订阅和节点授权。
