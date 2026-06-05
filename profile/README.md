<div align="center">

# Neul Labs

**High-performance infrastructure for AI agents.**

We build the fast parts of the AI stack. Rust-accelerated drop-in replacements for the tools agents actually depend on — LLM gateways, workflow engines, package managers, and developer tooling. Zero config. No rewrites. Just faster.

[Website](https://www.neullabs.com) · [Docs](https://docs.neullabs.com) · [Support](mailto:support@neullabs.com)

29 public projects · MIT/Apache 2.0

</div>

---

## Flagship

<div align="center">

**🌟 [Regulus](https://github.com/neul-labs/regulus) — The EU & UK compliance plane for Google ADK.**
Runtime `BasePlugin` suite encoding 10 regulations (EU AI Act, GDPR, DORA, NIS2, EHDS, UK GDPR, FCA SYSC, PRA SS1/23, PRA SS2/21, NHS DSPT) and 6 governance frameworks as runtime profiles. Hash-chained audit envelopes, PII redaction, dual-control kill switch, fail-closed data residency.
`Java 21` · `Maven` · [regulus-ai-adk-plugins](https://central.sonatype.com/namespace/com.neullabs) · [Repo](https://github.com/neul-labs/regulus)

</div>

---

## 🦀 Rust-accelerated drops-ins for Python stacks

The agent stack is built on Python libraries that were never designed for production concurrency. We profile, rewrite the hot path in Rust, ship as a drop-in replacement. Your code doesn't change — it just gets faster.

| Project | What it accelerates | Speedup (per the project) |
|---|---|---|
| [fast-litellm](https://github.com/neul-labs/fast-litellm) | LiteLLM connection pooling, rate limiting | 3.2× pool, 2.8× rate limit |
| [fast-langgraph](https://github.com/neul-labs/fast-langgraph) | LangGraph checkpoint + state management | 700× checkpoint, 10–50× state |
| [fast-crewai](https://github.com/neul-labs/fast-crewai) | CrewAI serialization, tools, DB search | 34× / 17× / 11× |
| [fast-axolotl](https://github.com/neul-labs/fast-axolotl) | Axolotl LLM fine-tuning (dedup SHA256) | Multi-threaded, no OOM |
| [fastworker](https://github.com/neul-labs/fastworker) | Python background workers | No Redis. No RabbitMQ. |
| [ormai](https://github.com/neul-labs/ormai) | Agent DB access (LangGraph / PydanticAI / SQLAlchemy / Tortoise) | Safe text-to-SQL |
| [fastagentic](https://github.com/neul-labs/fastagentic) | Production runtime for PydanticAI / LangGraph / CrewAI / LangChain | Cached `run_id`, MCP server |

---

## 🤖 Agent infrastructure

| Project | Description |
|---|---|
| [mcp-pay](https://github.com/neul-labs/mcp-pay) | Payment awareness layer for MCP (Model Context Protocol). |
| [agentvfs](https://github.com/neul-labs/agentvfs) | Workspace runtime and execution boundary for AI agents. |
| [brat](https://github.com/neul-labs/brat) | Multi-agent harness for AI coding tools. Crash-safe state, parallel execution, one CLI. |
| [ringlet](https://github.com/neul-labs/ringlet) | One CLI to rule all your coding agents. Profile-isolated, cost-tracked. |
| [grite](https://github.com/neul-labs/grite) | The issue tracker that lives in your repo. Built for AI agents. |
| [memorg](https://github.com/neul-labs/memorg) | Give your LLM a memory that actually works. |
| [stratafs](https://github.com/neul-labs/stratafs) | A semantic filesystem that turns file storage into a searchable knowledge base. |
| [openclawOS](https://github.com/neul-labs/openclawOS) | OS-like architecture for AI assistants with kernel-based, process-isolated applications. |
| [openclawMU](https://github.com/neul-labs/openclawMU) | Multi-tenant fork of OpenClaw with strict data isolation. |
| [openclaw-rs](https://github.com/neul-labs/openclaw-rs) | Community Rust implementation of OpenClaw. |
| [ukkin](https://github.com/neul-labs/ukkin) | Create AI agents on your phone that automate your daily tasks. |
| [m9m](https://github.com/neul-labs/m9m) | The n8n alternative without the bugs — faster, more reliable workflow automation in Go. |

---

## 🛠️ Developer tools (Rust rewrites of CLI classics)

| Project | Description |
|---|---|
| [gity](https://github.com/neul-labs/gity) | Make large Git repositories feel instant. |
| [stout](https://github.com/neul-labs/stout) | Stout is a drop-in replacement for the Homebrew CLI that's 10–100× faster for most operations. |
| [stout-index](https://github.com/neul-labs/stout-index) | Pre-computed package index for [stout](https://github.com/neul-labs/stout). |
| [rjest](https://github.com/neul-labs/rjest) | A blazing-fast Jest-compatible test runner. 100× faster warm runs. Zero config changes. |
| [rpytest](https://github.com/neul-labs/rpytest) | Run your pytest suite faster. Change nothing. |
| [rninja](https://github.com/neul-labs/rninja) | Build faster. Cache smarter. Drop-in ready (Ninja replacement). |
| [recurl](https://github.com/neul-labs/recurl) | curl that just works. Drop-in replacement with automatic anti-bot bypass. |
| [rewget](https://github.com/neul-labs/rewget) | wget, but it works everywhere. |
| [stkd](https://github.com/neul-labs/stkd) | Stacked Diffs for GitHub and GitLab (Graphite-compatible). |

---

## Why we exist

The AI agent stack is built on Python libraries that were never designed for production concurrency. LiteLLM's connection pool uses stdlib locks. LangGraph checkpoints serialize through a single thread. Package managers shell out to Ruby. The result: agents that work great in a demo and fall over in production.

We fix these bottlenecks one at a time: profile, rewrite the hot path in Rust, ship as a drop-in replacement. Your code doesn't change. It just gets faster.

## Contributing

Every project is MIT or Apache 2.0 licensed and accepts contributions. See the individual repository for setup instructions.

## Contact

[support@neullabs.com](mailto:support@neullabs.com) · [neullabs.com](https://www.neullabs.com) · [docs.neullabs.com](https://docs.neullabs.com)
