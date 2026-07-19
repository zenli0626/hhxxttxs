# Agents — 编排与自治

Durable, dated learnings that compound over time — one bullet per distilled
insight, sourced back to the issue it came from. Append-only; never edit past
entries, only add new ones below.

<!-- format: - **YYYY-MM-DD** — insight. ([source](url)) <!-- id:HASH --> -->
- **2026-07-16** — OpenAI 把 computer-use 正式装进 ChatGPT 桌面版：in-app browser、Chrome 扩展接管标签页、macOS 上有独立光标可后台操作，验证了「代理操作真实界面」已是产品级方向 ([source](https://mrqb.space/?d=2026-07-16)) <!-- id:2026-07-16-dfcd5b2d -->
- **2026-07-16** — Cua (Computer-Use 2.0)：accessibility-tree 优先、像素兜底、把操作范围限定在单个窗口而不是整个桌面 → 通过率 62%→80%，token -34%。对做屏幕代理的团队，这验证了「窗口级捕获」是对的方向；常缺的一环是 accessibility 层 ([source](https://mrqb.space/?d=2026-07-16)) <!-- id:2026-07-16-567580ae -->
- **2026-07-18** — Sachin Gupta 的 Feature Flags 给了一句可迁移的运营口径：『2026 是采纳，2027 是控制』，和一条最小起手式：先装 kill switch（全局 + 每工具），秒级生效、不用部署。一条易被忽略的铁律：所有派生出去的 worker agent 必须走同一层中间件，否则你刚按下的急停根本传不到派生出去的子进程。 ([source](https://mrqb.space/?d=2026-07-18)) <!-- id:2026-07-18-8dba219c -->
