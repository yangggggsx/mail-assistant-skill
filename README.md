# Mail Assistant Skill

云端邮件助手的完整 Codex Skill 包，私有保存。

## 下载与安装

下载本仓库的 **mail-assistant-skill.zip** 并解压。完整源码和目录结构保存在 ZIP 内（当前网页上传版本采用压缩包分发）。

将解压后的 `mail-assistant-skill/skills/mail-assistant` 目录复制到 `~/.codex/skills/mail-assistant`，重新加载技能。若已有同名技能，请先备份。

然后对 Codex 说：`使用 $mail-assistant，检查配置并协助部署邮件助手。`

安装 Skill 不会自动部署服务。需要配置自己的 Cloudflare、邮箱 OAuth、OpenAI 和 Pushover。包内没有生产密钥、私人邮件、数据库备份或个人访问链接。

## 包内内容

- Gmail / Outlook 收件、分类、摘要、推送、翻译与反馈。
- iPhone 快捷指令添加提醒事项及结果回传。
- 邮件、PDF、图片（含 HEIC/HEIF）提取日程，可编辑预览后写入 Outlook。
- 完整 Worker 源码、145 项测试、部署配置生成器、部署及维护文档、云端结构图。

解压后阅读 README.md 和 skills/mail-assistant/references/deployment.md。

## 验证

145 项 Worker 测试、3 项配置生成器测试及 Skill 格式校验通过；新生成部署副本的测试和 Wrangler dry-run 通过。尚未以全新账号完成真实部署验收。

ZIP SHA-256：`6a1316033fb459d956727d344da2ecad2890abbe61a3655849c381658d826eb4`

当前没有开源许可证。此仓库上传不影响现有线上邮件助手。
