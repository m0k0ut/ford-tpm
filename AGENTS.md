# Agent Context — Ford TPM Application

## Role Being Applied For

**Position:** Technical Product Manager – VESSE Ecosystem of AI Tools
**Company:** Ford Motor Company
**Level:** Technical AI Product Manager

## Core Mission of the Role

Act as a technical PM, AI-native practitioner and internal evangelist to lead the strategy, rapid prototyping, and adoption of AI solutions that accelerate design, development, and validation of vehicle electrical, software, and systems engineering (VESSE) workflows.

The role is equal parts **AI Product Manager**, **hands-on prototyper**, and **change agent**.
The primary customers (users) are VESSE engineers.

---

## Key Responsibilities

### 1. Ecosystem Strategy & Evangelism

- Be the "product champion" for the VESSE AI tool suite
- Embed within engineering workflows to find pain points → translate to features
- Lead workshops, AMA sessions, and demos

### 2. Rapid POC Development (LCNC)

- Build quick "quick-win" POCs using AI-native tools (Streamlit, GitHub Copilot, Claude Code, Gemini, Google Antigravity, etc. )
- Validate feasibility and desirability before committing dev resources

### 3. Business Case & KPI Ownership

- Build business cases tied to VESSE metrics:
  - Engineering Hours Saved
  - Defect Detection Rate (DDR)
  - Time-to-Market reduction
  - System Reliability
- Report ROI directly to executive leadership

### 4. Technical Integration & Lifecycle Management

- Integrate AI tools with SysML, AUTOSAR, MBSE tools, and CI/CD pipelines
- Partner with data engineers for high-quality labeled training data

---

## Domain Jargon (Source of Truth)

| Term | Meaning |
|------|---------|
| **VESSE** | Vehicle Electrical, Software, or Systems Engineering — the department being served (the "customers") |
| **SDV** | Software-Defined Vehicle — cars whose features/performance are dictated by software, not hardware |
| **E/E Architecture** | Electrical/Electronic Architecture — the "nervous system" blueprint of how power and data flow in the car |
| **ECU** | Electronic Control Unit — mini-computers inside a car (100+ per modern vehicle) |
| **CAN / Ethernet** | Networks allowing ECUs to communicate; CAN = traditional/reliable, Automotive Ethernet = high-bandwidth (cameras, autonomous driving) |
| **MBSE** | Model-Based Systems Engineering — using visual digital models instead of Word documents to describe system behavior |
| **SysML** | Systems Modeling Language — the standard visual language for MBSE diagrams |
| **AUTOSAR** | Global standard for automotive software architecture ensuring cross-supplier software compatibility on any ECU |
| **LCNC** | Low-Code/No-Code — platforms (Streamlit, Claude, Gemini) to build apps quickly without heavy coding |
| **POC** | Proof of Concept — a quick prototype to validate an idea before full-scale development |
| **DDR** | Defect Detection Rate — a key KPI measuring how early defects are found |

---

## The Role's 5-Step Workflow (Plain Language)

1. **Find the Pain** — Sit with VESSE engineers, observe workflows, spot bottlenecks (e.g., "20 hrs to cross-reference requirements docs")
2. **Build a Quick POC** — Use AI-native tools (Claude/ChatGPT/Streamlit, etc) to build a 3-4 day prototype
3. **Sell the Idea** — Demo in AMA sessions; convince skeptical safety-focused engineers to trust AI
4. **Justify the Cost** — Build business case with KPIs (hours saved, defect rate, ROI) for leadership
5. **Scale It** — Hand POC + business case to full-stack devs/data engineers for production build

---

## Interview Focus Areas

- Product Discovery & User Empathy
- Change Management / Driving Adoption (engineers are resistant to new tools)
- Rapid Prototyping (POC experience)
- Measuring Success (KPIs tied to business metrics)
- Cross-Functional Collaboration (engineers ↔ leadership ↔ dev/data teams)

---

## Source Files (in `Files/`)

- `Files/job description.pdf` — Full job description with responsibilities, requirements, KPIs
- `Files/Ford TPM jargon.pdf` — Role breakdown, jargon guide, and practice interview questions

---

## Artifacts Being Built (in `web/`)

- `web/index.html` — Teaser webpage: understanding of space + working methodology + 90-day plan of action

---

## Design System (REQUIRED for all visual artifacts)

All visual work — webpages, slides, mockups, prototypes — MUST follow the **Ford "Reimagine" design system** stored in `design-system/`. This keeps every artifact consistent.

- **Rules & component specs:** `design-system/DESIGN_SYSTEM.md`
- **Design tokens (import directly):** `design-system/colors_and_type.css`
- **Core principle:** restraint and breathing room — remove don't add, show less larger, lean light and airy.
- **Key colors:** Ford Blue `#003478` (brand), Electric Blue `#066fef` (CTAs/links/accents), near-black `#00142e` / `#0b0c0e` (dark surfaces), white `#ffffff`.
- **Fonts:** Archivo Expanded (display), Archivo (body), JetBrains Mono — substitutes for Ford's Antenna / Ford F-1.
- **Buttons** are pill-rounded; **icons** are Lucide; **no emoji**; CTAs are Title Case verbs with trailing `›`.

## Agent Collaboration Notes

- `CLAUDE.md` and `GEMINI.md` are symlinks to this file — edit `AGENTS.md` to update all agents
- When building artifacts, reference this file for role context, jargon, KPIs, and responsibilities
- The webpage (`web/index.html`) is the primary deliverable — it should demonstrate PM thinking, domain fluency, and an AI-native approach
