# Tpool — Agent-Only 招聘数据平台 (Recruitment Data Platform for AI Agents)

**Tpool is a China-focused recruitment data platform built exclusively for AI agents.** It exposes structured job data — postings, campus hiring, announcements and HR rating dimensions — through a REST API and an MCP server. Tpool does not accept human signups, and it deliberately has **no résumé-submission / apply feature** (collected postings often lack employer mailboxes; applying is out of scope).

Tpool 是一个专供 AI Agent 使用的招聘数据平台：提供岗位、校招、公告与 HR 五维评分等结构化数据（REST API + MCP）。不对人类开放注册，且明确排除投递功能。

## Key facts / 数据规模

- 620,000+ job postings, 142,000+ companies, 36,000+ campus-recruiting positions（62 万+ 岗位 / 14.2 万+ 企业 / 3.6 万+ 校招）
- Read-only data access; agent identity via API Key (`tp_v1_*` header `X-API-Key`)
- Hybrid retrieval (keyword + vector) over the job corpus

## Access / 接入方式

| Entry | URL |
|---|---|
| Website | https://www.tpool.com.cn |
| REST API docs (OpenAPI) | https://www.tpool.com.cn/docs |
| MCP server (streamable-http) | https://www.tpool.com.cn/mcp |
| Agent onboarding (llms.txt) | https://www.tpool.com.cn/llms.txt |
| Agent install guide | https://www.tpool.com.cn/agent-install.md |

MCP: several tools are open without a key (meta, code_of_conduct, announcement_filters); retrieval tools require `X-API-Key`. Agents can register via `POST /api/v1/agent/register` to obtain a key.

MCP 说明：meta / code_of_conduct / announcement_filters 等工具免 Key；检索类工具需 `X-API-Key`（`tp_v1_` 前缀），Agent 可通过注册端点领取。
