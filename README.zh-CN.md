# 拒付证据包整理 Skill

[English](README.md) | [简体中文](README.zh-CN.md)

在争议截止日期前，整理更干净、更有证据支撑的 chargeback response。

本项目是 [实用 Agent Skills](https://github.com/oceanfsdfsvfdsvs/practical-agent-skills) 集合的一部分。

`chargeback-evidence-pack` 是一个本地优先的 agent skill，面向商家、电商运营、SaaS 创始人和支付运营团队。它帮助你整理拒付/争议所需的订单、履约、物流、条款接受和客户沟通证据，同时避免泄漏无关客户数据或敏感日志。

## 适用场景

- Product-not-received、digital goods、subscription、service disputes。
- 检查订单收据、物流记录、履约记录、条款接受、退款状态和客服沟通。
- 输出 challenge / accept 建议，并列出证据缺口。

## 为什么不只用普通 Prompt

- 按争议 reason code 组织证据。
- 在提交弱证据前标记缺口。
- 阻止上传完整卡号、凭据、原始私有日志或无关客户记录。
- 输出结构化证据清单，而不是一段泛泛的申诉文案。

## 运行示例

```bash
python3 scripts/chargeback_evidence_pack.py \
  --case scripts/fixtures/case_product_not_received.json \
  --evidence-dir scripts/fixtures/evidence
```

## 运行时说明

- Codex/OpenAI 风格 agents：使用 `SKILL.md` 和 `agents/openai.yaml`。
- Claude Code：使用 `.claude/skills/chargeback-evidence-pack/SKILL.md`。
- OpenClaw：查看 `openclaw/README.md`。

本地验证不需要支付处理商凭据或网络访问。
