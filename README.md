# Mail Assistant Skill

云端邮件助手的完整 Codex Skill 包，私有保存。

## 下载与安装

下载本仓库的 **mail-assistant-skill.zip** 并解压。完整源码和目录结构保存在 ZIP 内（当前网页上传版本采用压缩包分发）。

将解压后的 `mail-assistant-skill/skills/mail-assistant` 目录复制到 `~/.codex/skills/mail-assistant`，重新加载技能。若已有同名技能，请先备份。

然后对 Codex 说：`使用 $mail-assistant，检查配置并协助部署邮件助手。`

安装 Skill 不会自动部署服务。需要配置自己的 Cloudflare、邮箱 OAuth、OpenAI 和 Pushover。包内没有生产密钥、私人邮件、数据库备份或个人访问链接。

## iPhone 提醒事项快捷指令

[安装「邮件助手-加入待办」](https://www.icloud.com/shortcuts/7a610bc2e6524944ad34449f66d94e11)

安装后先创建自己的「邮件待办」列表，再打开快捷指令，在“添加提醒事项”动作里重新选择该列表。共享版本含作者设备上的列表引用，不能假定会自动匹配。保留快捷指令名称，并安装 Pushover，以便成功后返回该应用。

快捷指令从自己的邮件助手“加入待办”入口启动；不要直接点击运行空输入，也不要传入不明链接。2026-10-26 静态检查动作未发现固定服务器地址或 API 密钥；没有执行或验证新手机安装。PDF/图片上传快捷指令仍按包内文档单独配置。

## 包内内容

- Gmail / Outlook 收件、分类、摘要、推送、翻译与反馈。
- iPhone 快捷指令添加提醒事项及结果回传。
- 邮件、PDF、图片（含 HEIC/HEIF）提取日程，可编辑预览后写入 Outlook。
- 完整 Worker 源码、145 项测试、部署配置生成器、部署及维护文档、云端结构图。

解压后阅读 README.md 和 skills/mail-assistant/references/deployment.md。

## 验证

145 项 Worker 测试、3 项配置生成器测试及 Skill 格式校验通过；新生成部署副本的测试和 Wrangler dry-run 通过。尚未以全新账号完成真实部署验收。

ZIP SHA-256：`6197b2376eca564711f7b17766270838a8bd2ac1495025b898d1778a201dee8c`

当前没有开源许可证。此仓库上传不影响现有线上邮件助手。
