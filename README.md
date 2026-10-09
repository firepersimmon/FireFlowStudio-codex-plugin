# FireFlowStudio Marketplace

FireFlowStudio 的 Codex 插件目录，提供一个插件：[`fireflowstudio`](plugins/fireflowstudio)。在 Codex 中连接 FireFlowStudio 工作台，管理资产、生成剧本、推进剧本流程，并完成美术资产图片生成和视频生成。

| 安装标识 | 展示名 | 连接地址 | 版本 |
| --- | --- | --- | --- |
| `fireflowstudio` | FireFlowStudio | `https://localhost:8038/mcp` | `0.1.0` |

接入方式是 Codex 原生 HTTP Remote MCP：插件不预置 client ID、回调地址或凭据，也不含本地 server，客户端按服务端 OAuth 元数据完成注册与登录。

## 安装

本仓库公开可读，无需 GitHub 授权，本机 Git 能正常访问 GitHub 即可。

```bash
codex plugin marketplace add https://github.com/firepersimmon/FireFlowStudio-codex-plugin.git --ref main
codex plugin add fireflowstudio@fireflowstudio
```

装完重新加载插件或新建 Codex 任务，在 MCP 连接管理里对 `fireflowstudio` 完成 FireFlowStudio OAuth 登录即可使用。每位使用者用自己的 FireFlowStudio 账号完成授权。

也可以通过命令行发起登录：

```bash
codex mcp login fireflowstudio
```

## 更新

```bash
codex plugin marketplace upgrade fireflowstudio
codex plugin add fireflowstudio@fireflowstudio
```

更新后新建 Codex 任务验证。未授权时连接地址返回 `401` 并给出 `WWW-Authenticate: Bearer`，OAuth 资源元数据和授权服务器元数据端点返回 `200`，这是预期状态。
