# 🌀 MCH: CALL FOR ENGINEERS

**Matrice à coeur Haddock** is looking for a **true engineer**—not a startup founder, not a consultant, but someone who loves building **elegant, efficient systems** that actually work.

---

## Who We Are

We're building the **Unix/CERN philosophy** for modern AI:
- **Stateless, protocol-driven agents** (like HTTP was for the web)
- **Emoji-compressed language tokens** for edge AI (C64-tier efficiency on modern hardware)
- **Apache 2.0 licensed**, fully open, no cloud vendor lock-in
- **Decentralized by design**: runs on your laptop, your phone, your router—anywhere

Think: *"What if Unix pipes worked on concepts instead of text?"*

---

## The Role: Lead Systems Engineer

### What we need you to build (Phase 1: 8-12 weeks)

You'll implement the **core protocol stack**:

```
┌─────────────────────────────────────────┐
│  EmojicomValidator (token compression)  │
├─────────────────────────────────────────┤
│  MHCMatrix (manifold math + consensus)  │
├─────────────────────────────────────────┤
│  BOOP Protocol (stateless, JSON-based)  │
├─────────────────────────────────────────┤
│  CLI Tools (Unix-style composability)   │
├─────────────────────────────────────────┤
│  Docker + CI/CD (edge deployment)       │
└─────────────────────────────────────────┘
```

### Specific deliverables:

1. **`mch-core/`** — Python 3.11+ library
   - `emojicom.py` — Unicode validation, ZWJ attack prevention, token density control
   - `mhc_matrix.py` — Doubly-stochastic matrices, Sinkhorn constraints, geometric validation
   - `consensus.py` — Majority voting, manifold stability checks
   - Full test suite (pytest, coverage >90%)

2. **`mch-bin/`** — Three CLI tools (think `ls`, `cat`, `grep`)
   - `mch-validate` — Validate emoji tokens for injection/DoS
   - `mch-audit` — Run PME audit (the "Pito" commercial engine)
   - `mch-matrix` — Build/inspect MHC matrices

3. **`Dockerfile` + GitHub Actions**
   - Multi-arch build (amd64, arm64) — runs on Mac M1 and old PC
   - Auto-publish to GHCR on git tag
   - ~80MB final image (Alpine + Python slim)

4. **Documentation**
   - API reference (docstrings + generated Sphinx docs)
   - Architecture.md explaining Unix philosophy approach
   - Integration guide for future AI/robotics modules

---

## Why This Matters

### Energy efficiency (you care about climate? Here's proof)
- **Traditional cloud setup**: 47 microservices = 131 kWh/year
- **MCH on laptop**: `docker run` 5min/day = 0.3 kWh/year
- **Savings**: 430x less energy, 99.7% hardware idle time, RGPD-compliant (no data leaving device)

### Technical purity
- **No frameworks**. Just Python stdlib + NumPy + pytest.
- **No cloud SDKs**. Just HTTP (you build the server if needed).
- **No hidden dependencies**. Every line auditable.
- **Apache 2.0**. You own it. You fork it. You can sell derivatives.

### Real impact
- PMEs automate 3-5 processes with **12-month ROI** (€5k-€16k per process)
- Robotics teams use Emojicom tokens to control physical hardware (motors, sensors)
- Researchers fork it, add constraints, publish papers
- You build something that lasts 20+ years (like Apache itself)

---

## Required Skills

✅ **Must have:**
- Python 3.11+ (5+ years production code)
- NumPy/SciPy or PyTorch (matrix math, geometric constraints)
- Unix/Linux CLI design philosophy
- Docker + GitHub Actions (CI/CD)
- Git workflow (branching, PRs, semantic versioning)

✅ **Nice to have:**
- Rust (optional: performance-critical parts later)
- Unicode/UTF-8 security audit experience
- Small Language Model (SLM) integration (Llama, Claude Nano, etc.)
- IoT/robotics (ROS2, Arduino protocols)

❌ **Deal-breakers:**
- "I mostly use AWS/cloud SDKs"
- "Framework dependency is fine"
- No GitHub portfolio or open-source history
- Needs hand-holding (we're non-hierarchical, async-first)

---

## What We Offer

### Compensation
- **€25-35/hour** (or $30-40 USD) for the Phase 1 build (~300-400 hours = €7.5k-€14k total)
- **Equity option**: 5-10% of commercial future (if MCH monetizes via specializations)
- **Royalty** on any research papers/projects using your code

### Freedom
- **Work your hours**. Async communication (GitHub, Discord, email).
- **Keep your IP**. All contributions Apache 2.0. You can cite this work anywhere.
- **No pivot risk**. The license guarantees you can't lose this codebase.

### The vision
- You're not building for a job. You're building a **protocol** that outlasts companies.
- Think: "What if I designed the next HTTP?" (OK, maybe 1% of that impact 😉)

---

## How to Apply

**Send to**: etiennekossovsky@protonmail.com

**Subject**: `MCH Engineer Application - [Your Name]`

**Include**:
1. Brief intro (who you are, why MCH interests you)
2. GitHub profile or portfolio (show actual code)
3. 3-5 projects you're proud of (link + 2-3 sentence explanation)
4. Availability (hours/week, timezone, when you can start)
5. Any questions about the role

---

## Timeline

- **Week 1-2**: Onboard, architecture review, repo setup
- **Week 3-8**: Core implementation (emojicom + mhc_matrix + consensus)
- **Week 9-10**: CLI tools + Docker integration
- **Week 11-12**: Tests, docs, GitHub Actions, v0.1.0 release

**Target release**: June 2026

---

## Questions?

- **Technical questions**: Open an issue on the repo
- **Role questions**: Drop a comment in [Discussion #X] (TBD)
- **Confidential**: Email above

---

### The Pitch

*"MCH is Unix philosophy meets modern AI. You'll build the compression layer that lets edge devices run sophisticated agents without cloud."*

*"This isn't a startup. It's a protocol. And protocols outlast companies."*

---

🌀 **We're looking for someone who gets this.** Are you that person?

**[Apply Now](mailto:etiennekossovsky@protonmail.com)**
