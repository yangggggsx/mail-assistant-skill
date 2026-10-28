# Mail Assistant 邮件助手

个人独立部署的云端邮件助手 Codex Skill。**公开预览版：尚未完成独立新账户、真实 OAuth 和新手机的端到端验收，也未完成完整安全审计。** 当前不是支持公众注册的多租户服务。

## 使用许可

个人自用和修改免费，包括处理自己的工作邮件。售卖、收费代部署或利用本软件提供付费服务，需要作者事先单独书面商业授权，费用和范围另行约定。版权不随授权转让。修改版再分发及企业统一内部部署未获本许可证授权。

完整条款见 [LICENSE](LICENSE)。第三方组件适用各自许可证。本项目采用源码可见的个人使用许可证，不是允许自由商用的标准开源许可证。商业授权可通过本仓库 Issues 请求联系渠道；不要提交秘密或私人数据。

## 下载与安装

下载 [mail-assistant-skill.zip](mail-assistant-skill.zip)，解压后阅读包内 README.md、RELEASE_READINESS.md 和 skills/mail-assistant/references/getting-started.md。

完整源码、测试、锁文件和文档目前在 ZIP 内；GitHub 根目录暂采用 ZIP 分发，尚未完成正常源码目录迁移。迁移方案见包内 SOURCE_IMPORT.md，已有远端历史将保留。

将解压后的 `mail-assistant-skill/skills/mail-assistant` 整个目录（含 LICENSE）复制到 `~/.codex/skills/mail-assistant`，重新加载技能。已有同名技能时先检查和备份。

示例：

> 使用 $mail-assistant，检查配置并协助在我自己的账户部署邮件助手。

安装 Skill 不会自动部署服务。需自行准备 Cloudflare、邮箱 OAuth、OpenAI 和 Pushover；账户注册和 OAuth 由本人完成。当前生成器仍要求目标 Outlook 日历账户，并生成两个 Queue 和 Images 绑定；分阶段验收不代表已经支持精简安装模式。

## 功能与范围

- Gmail / Outlook 收件、邮件类别与重要程度双维度分类、摘要、Pushover 推送和简报。
- 中文翻译、分类反馈、复制到 AI 的上下文与反馈。
- iPhone 快捷指令「加入待办」写入 Apple 提醒事项并回传结果。
- 邮件、PDF、图片及 HEIC/HEIF 提取会议、活动、截止日期等日程；可编辑预览后确认写入 Outlook 并核验。
- 课程关联更新和 Outlook JunkEmail 云端复查；不据此宣称所有邮箱垃圾箱均覆盖。

Gmail / Outlook 直接授权接入无需自动转发。其他邮箱可考虑转发到已接入邮箱，具体受服务商和组织政策限制，原邮件定位与垃圾箱覆盖需实测。

当前通知渠道为 Pushover。飞书尚未适配；需要处理认证、消息布局、操作链接及快捷指令返回目标，不能只替换 API URL。

## iPhone 快捷指令

[安装「邮件助手-加入待办」](https://www.icloud.com/shortcuts/7a610bc2e6524944ad34449f66d94e11)。共享版本保留作者设备上的提醒事项列表引用，安装后必须在“添加提醒事项”动作里重新选择自己的「邮件待办」列表。保留快捷指令名称并安装 Pushover；从邮件助手的“加入待办”入口启动。

已做静态检查，未在新手机完成安装验收。PDF/图片上传快捷指令按包内 shortcuts.md 单独配置。创建日程或待办成功后默认不额外发送 Pushover 成功通知。

## 版本与验证

- 来源提交：`357a8f5f1fd08e2382c67910cbc4a04ebf99905c`（本地源码历史；与网页上传历史独立）。
- ZIP SHA-256：`d159b1fcec8e18f6edcfcf10472c2109daa61d404a4b118a681c7017668aa571`。
- [SHA256SUMS](SHA256SUMS) · [逐文件来源清单](source-manifest.json)。
- Worker 145 项模拟测试及配置生成器 4 项测试已通过；此前生成副本的 Wrangler dry-run 通过，详见包内 VALIDATION.md。
- 本次发布改动为打包、文档和许可，未修改或部署生产服务。模拟测试不能替代真实账户、通知、日历和手机验收。

升级回滚、异常重试、安全审查、私密漏洞报告渠道和独立账户验收仍待完成。不要在公开 Issues 发布密钥、OAuth 链接、私人操作链接、邮件、附件或完整日志；私密报告渠道尚未建立前仅提出联系请求。
