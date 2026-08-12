# DevOps Prompt Pack

8 specialist AI system prompts for DevOps engineers — Terraform, Kubernetes, CI/CD, and cloud ops. MIT licensed, plain Markdown.

## Why constraint-based prompts work

Positive instructions ("be secure", "follow best practices") don't change the output — the model already tries to be secure. What works is eliminating concrete failure modes by name.

**Real constraint block from the Terraform prompt:**

```
NEVER use floating image versions; pin + reference immutable tags
NEVER hardcode secrets; read from environment only
NO local state; remote state with locking required
Least-privilege IAM only; no wildcard actions or roles
Output plan-first for review; never auto-apply to production
```

Running this against Terraform generation tasks, the hardcoded-secrets failure dropped to near-zero. With a positive-only prompt, it appeared roughly 30% of the time.

## The 8 prompts in the pack

1. **IaC Generator** (Terraform/OpenTofu) — plan-first, no wildcards, remote state, least-privilege IAM
2. **Kubernetes Manifest Writer** — non-root containers, resource limits, no latest tags, health checks required
3. **CI/CD Pipeline Builder** (GitHub Actions/GitLab) — SHA-pinned actions, secret scanning, no hardcoded env
4. **Cloud Cost Optimizer** — quantified savings, rightsizing with evidence, no vague "optimize" suggestions
5. **Incident Responder** — timeline-first, no speculation, actionable remediations only
6. **Security Hardener** — OWASP/CIS-aligned, specific CVE references, no generic "add firewall" advice
7. **Monitoring Configurator** — SLO-first, alert fatigue prevention rules, no vanity metrics
8. **Runbook Writer** — step-by-step verification, rollback procedures required, no ambiguous steps

## What's different

These aren't "write me a Terraform module" prompts. Each one encodes how a staff DevOps engineer actually approaches the task — specialist vocabulary, domain-specific failure modes blocked, structured output format. The model stops guessing and starts constrained.

## Get the Full Pack

**[$29 on Gumroad](https://srmcguirt.gumroad.com/l/devops-prompt-pack)** — all 8 prompts, plain Markdown, MIT licensed. Works in Claude, GPT-4, Cursor, any tool that accepts system prompts. Yours to keep.

## Related tools

- [MCP Server Starter Kit](https://srmcguirt.gumroad.com/l/mcp-starter) — TypeScript MCP server with rate limiting + Docker (Free/$49)
- [FastMCP Python Boilerplate](https://srmcguirt.gumroad.com/l/fastmcp-python) — Pydantic v2 + rate limiter + structlog ($35)
- [Marketing Prompt Pack](https://srmcguirt.gumroad.com/l/marketing-prompt-pack) — SEO, email, ads, landing pages ($29)
- [MCP Vertical Server Bundle](https://srmcguirt.gumroad.com/l/mcp-vertical-bundle) — GitHub, Slack, Notion MCP servers ($99)

Full lineup: [wireforge.fellwork.workers.dev](https://wireforge.fellwork.workers.dev)

## License

MIT — use any prompt in production. No attribution required.
