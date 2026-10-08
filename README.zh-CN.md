# 相机卡片演示

English | [简体中文](README.zh-CN.md)

这是静态 OctoScript L0 相机界面，用于演示本地素材、中文文字和 App Hub 发布流程。相机样式的控件不会拍照或修改设置。应用不请求能力、不访问网络，也没有助手。

导出布局来自历史 Octoscript-AppCard 图像转卡片流程中的相机拍照场景。新版修正字体路径，使用可移植的内置中文字体。

## 源码与版本

可编辑应用位于 bundle/。PRIVACY.md 说明数据边界，review/ 在应用包外保存验收证据。新身份为 io.github.ymote.cameracard。历史 camera-card 版本保持原样且独立存在；新版不会更新已有安装。

首个目标平台是 macOS。Android 和其他平台需单独验收后才能加入商店描述。

## 发布

按照[提交指南](https://github.com/OctoSense-org/OctoSense-App-Hub/blob/main/docs/SUBMITTING.md)创建 [App Hub issue](https://github.com/OctoSense-org/OctoSense-App-Hub/issues)。issue 可以早于 release，需提供仓库、版本、权限、截图和当前验证状态。

tools/octo publish-github 安装的工作流会检查并证明新的 vVERSION 标签，随后生成 app.bundle.pack.json 和发布收据。无需开发者签名私钥或仓库签名密钥。仓库保留可编辑源码；审查和安装使用封装后的 release 包，不得重新计算它的摘要或移动旧标签。

release 成功不代表已获 Hub 接纳。将证据补充到 issue，由管理员审查确切候选后发布目录。安装需要支持 publisher-github-v1 的 OctoSense 宿主（应用契约 1.8.0）。

## 验证状态

未签名应用包已通过准入检查。在关闭系统字体发现的条件下，已查看 406 × 776 和 900 × 800 逻辑点的 macOS 原生截图。无效字体路径和导出尺寸缩小一半的问题已修正。这仍是固定画板的静态演示，宽窗口会有空白。GitHub 证明和公开 Hub 安装更新验收尚待完成，详见 review/ANSWERS.md；不会宣称具备实际拍照或账户连接能力。
