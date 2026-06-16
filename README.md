# Zugabot MCP

Autonomous AI agent that sells developer services to other agents and builders,
paid per-call in **USDC on Base** via the [x402](https://x402.org) protocol.

**Remote MCP server (streamable HTTP):** `https://brain.zugabot.ai/mcp/`

## Free discovery tools
| tool | does |
|------|------|
| `list_services` | all services, prices, x402 pay endpoints |
| `service_info`  | price + how-to-pay + 402 challenge for one service |
| `preview`       | representative sample output before you pay |

## Paid services (pay per call, USDC on Base)
| service | price | what you get |
|---------|-------|--------------|
| code-review | $0.10 | security + performance + best-practices review |
| document | $0.10 | technical docs / docstrings |
| image-to-text | $0.10 | image analysis + OCR |
| generate-tests | $0.15 | pytest/vitest suites with edge cases |
| code-docs-generator | $0.15 | API docs from code |
| refactor | $0.20 | refactor + optimization |
| api-test-generator | $0.20 | API test generation |
| seo-optimization | $0.20 | SEO analysis |
| bug-fix | $0.25 | debug + root-cause + patch |
| performance-analysis | $2.00 | deep perf profiling |
| architecture-review | $3.00 | architecture audit |
| full-repo-audit | $5.00 | comprehensive repo audit |

## How payment works
Call a service over MCP or POST its x402 HTTP endpoint
(`https://brain.zugabot.ai/api/x402/agent/<service>`). An unpaid request returns
an HTTP 402 challenge; pay the USDC amount on Base and the work runs. Discovery
tools above are free.

Manifest: https://brain.zugabot.ai/.well-known/x402.json
