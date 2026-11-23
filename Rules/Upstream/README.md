# Rules/Upstream | 上游规则镜像

把配置里订阅的上游分流规则原样备份到本仓库，上游删库、下线也不怕。
每天 02:00（北京时间）由 `.github/workflows/mirror-upstream-rules.yml` 自动拉取更新，
也可以在 GitHub Actions 里手动跑一次。

| 文件 | 上游来源 | 配置里的策略 |
|---|---|---|
| AmazonCN.lsr | rule.kelee.one/Loon/AmazonCN.lsr | DIRECT |
| Amazon.lsr | rule.kelee.one/Loon/Amazon.lsr | DIRECT |
| Microsoft.lsr | rule.kelee.one/Loon/Microsoft.lsr | DIRECT |
| GitHub.lsr | rule.kelee.one/Loon/GitHub.lsr | 时延优选 |
| AppleFirmware.lsr | rule.kelee.one/Loon/AppleFirmware.lsr | DIRECT |
| TikTok.lsr | rule.kelee.one/Loon/TikTok.lsr | DIRECT |
| Gemini.lsr | rule.kelee.one/Loon/Gemini.lsr | PROXY-AI |
| filter.lsr | fmz200/wool_scripts filter.list | REJECT |
| AppStore.lsr | rule.kelee.one/Loon/AppStore.lsr | DIRECT |
| Twitter.lsr | rule.kelee.one/Loon/Twitter.lsr | 时延优选 |
| Instagram.lsr | rule.kelee.one/Loon/Instagram.lsr | 时延优选 |
| Telegram.lsr | rule.kelee.one/Loon/Telegram.lsr | 时延优选 |
| Threads.lsr | rule.kelee.one/Loon/Threads.lsr | 时延优选 |
| Tencent.lsr | rule.kelee.one/Loon/Tencent.lsr | DIRECT |
| WeChat.lsr | rule.kelee.one/Loon/WeChat.lsr | DIRECT |
| AI.lsr | fmz200/wool_scripts Loon/rule/AI.list | PROXY-AI（配置里已禁用） |
| Global.lsr | rule.kelee.one/Loon/Global.lsr | 时延优选 |
| ChinaMax.lsr | rule.kelee.one/Loon/ChinaMax.lsr | DIRECT |
| LAN_SPLITTER.lsr | kelee.one/Tool/Loon/Lsr/LAN_SPLITTER.lsr | DIRECT |
| REGION_SPLITTER.lsr | kelee.one/Tool/Loon/Lsr/REGION_SPLITTER.lsr | DIRECT |
| Apple.lsr | rule.kelee.one/Loon/Apple.lsr | DIRECT |
| iCloud.lsr | rule.kelee.one/Loon/iCloud.lsr | DIRECT |
| UnionPay.lsr | rule.kelee.one/Loon/UnionPay.lsr | DIRECT |
| MeiTuan.lsr | rule.kelee.one/Loon/MeiTuan.lsr | DIRECT |
| HeMa.lsr | rule.kelee.one/Loon/HeMa.lsr | DIRECT |
| FeiZhu.lsr | rule.kelee.one/Loon/FeiZhu.lsr | DIRECT |
| Duolingo.lsr | rule.kelee.one/Loon/Duolingo.lsr | DIRECT |
| DouBan.lsr | rule.kelee.one/Loon/DouBan.lsr | DIRECT |
| ChinaTelecom.lsr | rule.kelee.one/Loon/ChinaTelecom.lsr | DIRECT |
| ByteDance.lsr | rule.kelee.one/Loon/ByteDance.lsr | DIRECT |
| BiliBili.lsr | rule.kelee.one/Loon/BiliBili.lsr | DIRECT |
| Baidu.lsr | rule.kelee.one/Loon/Baidu.lsr | DIRECT |
| Alibaba.lsr | rule.kelee.one/Loon/Alibaba.lsr | DIRECT |
| AliPay.lsr | rule.kelee.one/Loon/AliPay.lsr | DIRECT |
| Douyin.lsr | fmz200/wool_scripts Loon/rule/Douyin.list | DIRECT |
| XiaoHongShu.lsr | rule.kelee.one/Loon/XiaoHongShu.lsr | DIRECT |
| Xunlei.lsr | rule.kelee.one/Loon/Xunlei.lsr | DIRECT |
| AppleMusic.lsr | rule.kelee.one/Loon/AppleMusic.lsr | DIRECT |
| GoogleVoice.lsr | rule.kelee.one/Loon/GoogleVoice.lsr | United States |

引用自己仓库的镜像时，把配置 `[Remote Rule]` 里的上游地址换成
`https://raw.githubusercontent.com/tomopte/Loon/main/Rules/Upstream/<文件名>.lsr`，
策略和 tag 保持上表不变。
