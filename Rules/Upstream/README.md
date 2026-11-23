# Rules/Upstream | 上游规则镜像

把配置里订阅的上游分流规则原样备份到本仓库，上游删库、下线也不怕。
每天 02:00（北京时间）由 `.github/workflows/mirror-upstream-rules.yml` 自动拉取更新，
也可以在 GitHub Actions 里手动跑一次。

注意：不镜像 kelee.one 的内容，配置里继续直接订阅上游地址。

| 文件 | 上游来源 | 配置里的策略 |
|---|---|---|
| filter.lsr | fmz200/wool_scripts filter.list | REJECT |
| AI.lsr | fmz200/wool_scripts Loon/rule/AI.list | PROXY-AI（配置里已禁用） |
| Douyin.lsr | fmz200/wool_scripts Loon/rule/Douyin.list | DIRECT |

引用自己仓库的镜像时，把配置 `[Remote Rule]` 里的上游地址换成
`https://raw.githubusercontent.com/tomopte/Loon/main/Rules/Upstream/<文件名>.lsr`，
策略和 tag 保持上表不变。
