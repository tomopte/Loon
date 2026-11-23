# Rules | 分流规则

按用途分门别类，Loon 配置里用远程规则引用，不用再写一堆本地规则。

| 文件 | 用途 | 策略 |
|---|---|---|
| Muse-US.lsr | Muse / Meta AI | United States |
| CN-AI-Direct.lsr | 中国 AI | DIRECT |
| AI-Proxy.lsr | Google 全家 + 国外 AI | PROXY-AI |
| Meta.lsr | Meta 全家（除 Muse/Meta AI） | 时延优选 |
| Direct.lsr | 苹果、多邻国、抖音相关等 | DIRECT |
| Reject.lsr | 开屏广告与广告域名 | REJECT / reject-dict |

在 Loon 配置的 `[Remote Rule]` 里按下面顺序添加（顺序就是匹配顺序）：

```
https://raw.githubusercontent.com/tomopte/Loon/main/Rules/Muse-US.lsr, policy=United States, tag=Muse-US, enabled=true
https://raw.githubusercontent.com/tomopte/Loon/main/Rules/CN-AI-Direct.lsr, policy=DIRECT, tag=CN-AI-Direct, enabled=true
https://raw.githubusercontent.com/tomopte/Loon/main/Rules/AI-Proxy.lsr, policy=PROXY-AI, tag=AI-Proxy, enabled=true
https://raw.githubusercontent.com/tomopte/Loon/main/Rules/Meta.lsr, policy=时延优选, tag=Meta, enabled=true
https://raw.githubusercontent.com/tomopte/Loon/main/Rules/Direct.lsr, policy=DIRECT, tag=Direct, enabled=true
https://raw.githubusercontent.com/tomopte/Loon/main/Rules/Reject.lsr, policy=REJECT, tag=Reject, enabled=true
```

本地 `[Rule]` 只留 Muse 那三条置顶和 `FINAL,时延优选` 即可。
