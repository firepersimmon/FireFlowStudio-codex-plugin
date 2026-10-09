# FireFlowStudio for Codex

在 Codex 中连接 FireFlowStudio 工作台，通过对话处理项目、资产、剧本和图片视频生成任务。具体可用操作以连接后提供的工具和你授予的权限为准。

- 插件名称：FireFlowStudio
- 安装标识：`fireflowstudio@fireflowstudio`
- 版本：`0.1.0`
- [官方网站](https://www.persfireai.com)

## 安装

在终端执行：

```bash
codex plugin marketplace add https://github.com/firepersimmon/FireFlowStudio-codex-plugin.git --ref main
codex plugin add fireflowstudio@fireflowstudio
```

安装后重新加载插件或新建 Codex 任务。

## 连接账号

1. 在 Codex 的 MCP 连接管理中找到 FireFlowStudio，发起登录。
2. 在打开的浏览器页面中登录你的 FireFlowStudio 账号。
3. 选择要授权的租户，并勾选允许应用使用的权限。
4. 点击同意授权，完成后返回 Codex 即可继续使用。

每位使用者使用自己的账号授权。你可以拒绝授权，也可以只选择需要的权限。应用实际可执行的操作仍受你在租户和项目中的业务权限限制。

## 使用

连接后，可以在对话中说明你要处理的项目和目标，例如：

- 查看项目和资产。
- 整理剧本与制作流程。
- 查询图片或视频生成任务的进度。

## 更新

```bash
codex plugin marketplace upgrade fireflowstudio
codex plugin add fireflowstudio@fireflowstudio
```

更新后重新加载插件或新建 Codex 任务。如果 Codex 提示需要登录，按页面提示重新连接账号。
