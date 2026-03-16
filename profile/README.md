# .principles

**Give your AI coding agent the mindset of a principled software engineer.**

Modern AI coding agents already know SOLID, GoF, OWASP, DDD, Clean Architecture, 12-Factor, and the rest. That's not the bottleneck. The bottleneck is that *knowing* all of this is not the same as *applying* the right subset of it to your specific codebase, your specific stack, and your specific risk profile.

`.principles` bridges that gap. It doesn't teach the AI — it gives it **intent**.

> 🎯 The AI writes the code. You bring the craft.

---

## 💡 The problem

When an AI agent opens your file, it doesn't automatically know:

- Should it focus on **security** here? *(Payment handler or utility?)*
- Should **DDD aggregates** guide this design? *(Rich domain or thin CRUD?)*
- Are **concurrency principles** critical here? *(Hot multithreaded path or single-user flow?)*
- Is **backward compatibility** a hard constraint? *(Public API or internal module?)*

Without context, the AI picks reasonable defaults. *Reasonable defaults are not your architecture.*

---

## 🌳 How it works

Place `.principles` files in your project — just like `.gitignore`, they cascade down the file tree and subdirectories can add, narrow, or suppress:

```
my-project/
├── .principles                ◄ 🌐 @microservices + @security-focused
├── backend/
│   ├── .principles            ◄ ☕ @spring-boot  (Java · REST · DDD)
│   └── src/payments/
│       └── .principles        ◄ 💳 CODE-RL-IDEMPOTENCY
├── frontend/
│   └── .principles            ◄ ⚛️  @react + @typescript
└── infra/
    └── .principles            ◄ 🏗️  @terraform + @twelve-factor
```

Before coding or reviewing, the AI walks up from the file to the git root, merges the hierarchy (innermost wins), and loads the full principle content into its context — front-of-mind, the way a senior developer carries their internalized knowledge into every session.

---

## 🔄 The workflow

```
🔭 /scout  →  ⚡ /prime  →  ✍️ code  →  🔎 /audit  →  🔧 fix  →  🔎 /audit  →  ✅ done
```

These are **AI commands, not CLI tools** — you use natural language:

| Command                     | What it does                                                                     |
|-----------------------------|----------------------------------------------------------------------------------|
| `/scout`                    | Analyzes your project, detects stack and domain, writes `.principles` files      |
| `/prime`                    | Loads the full principle hierarchy into the AI's context before you write a line |
| `/audit current changes`    | Reviews only what changed since last commit, grouped by severity                 |
| `/audit the payment module` | Reviews a specific area — you describe it, the AI finds it                       |

`/prime` is the shift-left move: principles active *while* you code, not just *after*. `/audit` is the quality gut-check — not just bugs, but *"is this code well-principled?"*

---

## 📚 What's included

214+ principles across 13 categories, actively growing:

**SOLID · Gang of Four · GRASP · DRY · KISS · YAGNI · Clean Architecture · DDD · CQRS · Event Sourcing · 12-Factor · OWASP Top 10 · Concurrency · Performance · Observability · API Design · Testing Strategy · and more**

Every principle cites a verifiable source — book with ISBN, RFC, or paper with DOI. Shipped groups (`@spring-boot`, `@react`, `@microservices`, `@security-focused`, …) bundle related principles for common stacks. Many principles include **code examples and diagrams** — not just a definition, but a demonstration of the principle in practice.

New namespaces in progress: functional programming, continuous delivery, database design, hexagonal architecture, threat modelling, and more. See [TODO.md](https://github.com/code-principles/.principles/blob/main/TODO.md).

---

## 📦 Repositories

- [**.principles**](https://github.com/code-principles/.principles) — the principle catalog, groups, layer model, and slash commands

---

## Status

Proof of concept — errors exist, gaps exist, groupings are opinionated. See the [Disclaimer](https://github.com/code-principles/.principles/blob/main/DISCLAIMER.md). Contributions are welcome.

