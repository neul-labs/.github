# Neul Labs

**High-performance infrastructure for AI agents.**

We build the fast parts of the AI stack. Rust-accelerated drop-in replacements for the tools agents actually depend on — LLM gateways, workflow engines, package managers, and developer tooling. Zero config. No rewrites. Just faster.

[Website](https://www.neul.uk) · [PyPI](https://pypi.org/project/fast-litellm/)

---

## Projects

### brat

**Multi-agent harness for AI coding tools.** Crash-safe state, parallel execution, one CLI. Orchestrates Claude Code, Aider, OpenCode, Codex, and others through a unified workflow layer backed by an append-only event log.

```
cargo install --path crates/brat
brat mayor start
brat witness run --once
```

`Rust` · [Repository](https://github.com/neul-labs/brat)

---

### fast-litellm

**Rust acceleration for LiteLLM.** Drop-in. 3.2× faster connection pooling. 2.8× faster rate limiting. Built with PyO3 and DashMap lock-free data structures. Import it and everything speeds up.

```python
import fast_litellm   # that's it
import litellm        # now Rust-accelerated
```

`Rust` `Python` · [Repository](https://github.com/neul-labs/fast-litellm) · [PyPI](https://pypi.org/project/fast-litellm/)

---

### fast-langgraph

**Rust accelerators for LangGraph.** Up to 700× faster checkpoint operations. 10–50× faster state management. Drop-in components for production agent workflows that need to be fast and crash-safe.

`Rust` `Python` · [Repository](https://github.com/neul-labs/fast-langgraph)

---

### gity

**Make large Git repositories feel instant.** A lightweight daemon that watches your files via OS-native watchers, implements Git's fsmonitor protocol, and caches status results. `git status` in milliseconds instead of seconds.

```
cargo install --path crates/gity
gity register /path/to/large-repo
git status   # fast
```

`Rust` · [Repository](https://github.com/neul-labs/gity)

---

### stout

**A drop-in replacement for the Homebrew CLI.** 10–100× faster for most operations. Pre-computed SQLite index with FTS5 full-text search, parallel bottle downloads, Ed25519 signed updates, and built-in CVE auditing. Works alongside existing `brew` installations.

```
stout install jq     # instant
stout search json    # instant
stout audit          # check for CVEs
```

`Rust` · [Repository](https://github.com/neul-labs/stout)

---

### fastworker

**Background workers for Python applications.** Add task queues in seconds, without the complexity of Celery or RQ.

`Python` · [Repository](https://github.com/neul-labs/fastworker)

---

## Why

The AI agent stack is built on Python libraries that were never designed for production concurrency. LiteLLM's connection pool uses stdlib locks. LangGraph checkpoints serialize through a single thread. Package managers shell out to Ruby.

We fix these bottlenecks one at a time: profile, rewrite the hot path in Rust, ship as a drop-in replacement. Your code doesn't change. It just gets faster.

---

## Contributing

Every project is MIT-licensed and accepts contributions. See the individual repository for setup instructions.

## Contact

[hello@neul.uk](mailto:hello@neul.uk) · Built in St Andrews, Scotland.
