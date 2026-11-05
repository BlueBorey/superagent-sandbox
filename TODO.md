# 待办

这个文件是 dsh-superagent 唯一的数据源。它不读日历、不读邮件、不读飞书任务，只读这里和这个仓库的 issue。
想让它干什么，写在这里，然后在飞书里说一句「按 TODO.md 干」。

## 今天

- [ ] 给智能体一个独立 GitHub 账号。它现在 commit 和开 PR 用的都是 BlueBorey 本人身份，和你的账号分不开。
- [ ] 用 Borey78 发一条真实 issue 验收 GitHub 入口。自己账号 BlueBorey 发的 issue 它不接（源码里跳过自己创建的单）。
- [ ] 清掉仓库遗留：关闭 issue #1 #2 #4 #6（都是早期试跑），处理 PR #5 #8（都停在 open）。
- [ ] 决定 `windows-adaptation.patch` 的去向。6 个源文件 +127/−21 是 Windows 上跑通必需的改动，现在只在本机工作树里，没提上游。

## 这周

- [ ] 飞书应用补 `task:task:read`。想让它读飞书待办才需要，不补也能用。
- [ ] 决定本机那套（3082）留作备胎还是停掉。现在 GitHub 和飞书入口都关着，只剩 runtime 在跑。
- [ ] 决定要不要开「不用 @ 也能触发」。开了之后你在群里正常说话它就接，代价是它可能自作主张。

## 已完成

- [x] 飞书入口搬到云端 ECS，独立应用 DSH Superagent
- [x] 两个模型网关（wb-proxy / 小布）搬到 ECS
- [x] 研判和执行拆两个模型：研判 `deepseek-v4.1-flash`，执行 `gpt-6-luna`
- [x] 修掉工作目录为空的问题（`executor.prepare` 曾是空字符串）
- [x] 面板隧道脚本，双击即可看云端面板
- [x] prompts 到 revision 3：待办只认本文件，不再反问用户数据存在哪
