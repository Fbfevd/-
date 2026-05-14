如何选择？

Claude Code 内部使用 MAX：选 vip_1_max；如果是高并发分发场景，选 vip_1_max_enterprise
外接应用或需要 1M 上下文：选 vip_1_max_ext；如果是普通低价外接，也可以考虑 free_2 或 free_2_new
直接走 Claude API：选 vip_1_api；如果是 AWS / Vertex 混合场景，选 vip_1_api_mix
Codex CLI 或外接 Codex：使用 vip_2；如需在 Claude Code 中调用 OAI 系列模型，使用 vip_2_cc
Gemini 模型：使用 vip_3 分组
Grok 或国产模型：分别使用 grok、vip_4 对应专用分组
如果你接的是 OpenClaw、第三方平台、网关、自定义客户端或其他外接场景，还需要按接入类型补对应的 User-Agent。完整规则见 外接调用 User-Agent 说明。