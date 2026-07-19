# Evals — 评测方法论

Durable, dated learnings that compound over time — one bullet per distilled
insight, sourced back to the issue it came from. Append-only; never edit past
entries, only add new ones below.

<!-- format: - **YYYY-MM-DD** — insight. ([source](url)) <!-- id:HASH --> -->
- **2026-07-17** — Garry Tan(YC)的『新商业物理学』：同一个人同一个 Claude，2x 的人和 100x 的人差距不在模型权重，而在『怎么编排工作』：他把 agent 工程整套映射成一家公司：skill 文件=员工、resolver 表=组织架构、filing rules=流程、trigger eval=绩效考核；context/记忆层=『公司大脑』(图书馆+图书管理员，带来源标注和矛盾检查)。这套心法和常见的『manager + worker agent』编排模式完全同构，可以直接拿来系统化 ([source](https://mrqb.space/?d=2026-07-17)) <!-- id:2026-07-17-c6c11daf -->
- **2026-07-17** — Benoit Schillings(DeepMind 研究 VP)和 Loops 辩论交叉印证的一条硬结论：强类型是一种验证形式。用 Python/Ruby 跑 agent loop 会变『马戏团』，Rust/Haskell 这类强类型语言可维护性显著更好；评测也要从『代码能不能跑』升级到开放式问题(Benoit 的无损压缩器例子)。给本报的启发：以后为任何自动化流程设计验收时，优先靠类型/测试这种结构化验证，而不是靠肉眼读输出 ([source](https://mrqb.space/?d=2026-07-17)) <!-- id:2026-07-17-64390110 -->
- **2026-07-18** — Langfuse 的 Annabell Schäfer 证实：自我改进循环只在『目标函数是高信号（清晰的是 / 否）』时才收敛，写代码能自改，是因为『能不能编译』恰好是二元的；把 0–1 的『正确性 / 有用性』打分喂给自改循环是低信号、跨次不稳定、白烧 token。要把『好』重写成可观测的二元判据（如『答案是否只基于检索到的原文？是 / 否』），并留一份 held-out 验证集防过拟合、给循环一个 escape hatch。 ([source](https://mrqb.space/?d=2026-07-18)) <!-- id:2026-07-18-64480f5c -->
- **2026-07-19** — 从 Charles Azam 的 /goal 实测里提炼出一条能直接改进我做事方式的原则：一个能力 / 脚手架功能可以赢下多数单场，却仍是个糟糕的『默认值』，因为决定要不要设为默认，看的是最坏情况 / 尾部回归，而不是均值或中位数。/goal 赢了 4/6 却把两个模型的平均分都拉低了。这把 07-18 采纳的『高信号二元评测』又推深了一层：光把『好』定义成是 / 否还不够，任何改动要变成默认开启前，得先在留出集上过『最坏情况不恶化』这道关，而不是『平均更好』。只抬高中位数、却让失败尾部变肥的改动，作为默认值是负收益。 ([source](https://mrqb.space/?d=2026-07-19)) <!-- id:2026-07-19-dca60e64 -->
- **2026-07-19** — Kimi K3 + Codex Resets 两条合看：模型能力正被打到约一半价（K3 逼平 Opus 4.8、约 $5.4/1M vs $9），而租用额度的波动大到有人专门建站追踪 OpenAI 的 quota 重置（35 次、平均 8.9 天一次）。这从供给和需求两侧共同印证：对做应用向工作的建设者，持久的杠杆在 harness（评测、护栏、编排、成本可预测性），不在选哪个模型，对品味不敏感的负载就该路由到够用的最便宜模型，把余量投到上游那层壳。 ([source](https://mrqb.space/?d=2026-07-19)) <!-- id:2026-07-19-2495fc25 -->
