# JARVIS Research — 01_PLAN.md
**Document Version**: 1.0.0  
**Phase**: Phase 1 — Comprehensive Research & Architecture Plan  
**Gate**: Human Approval Gate (Amit ki "haan" ka intezaar)  
**Rule**: Phase 2 will NOT start until Amit explicitly reviews and confirms this plan.  

---

## 1. Execution Order & Batch Architecture

Total 71 unique items ko logical architectural dependency ke hisaab se 3 discrete batches mein research kiya jayega. Har batch ke baad `research/PROGRESS.md` update hoga aur chat mein 5-line status snapshot aayega.

```mermaid
flowchart TD
    subgraph Batch1 ["BATCH 1: Core Intelligence & Control (31 Items)"]
        B1_Mem["Memory (5 Items)<br/>Honcho, mem0, Codebase Memory, claude-mem, Second Brain"]
        B1_Ctrl["Computer & Phone Control (7 Items)<br/>Agent Desktop, Coucou, Atticus-mac, OpenBot, Expo, CLI-Anything, Barehands"]
        B1_Brw["Browser Control (2 Items)<br/>browser-use, openmuse"]
        B1_Bots["Bots & Multi-Agent (17 Items)<br/>OpenMausBot, Mark-LVI, OpenJarvis, adewaskar, deer-flow, agency-agents, OpenDevin, fullstack-agent, OpenDots, OpenTag, Orca, Hermes, Herdr, Executive Assistant, Content Agent, Chief of Staff, sellbird"]
    end

    subgraph Batch2 ["BATCH 2: Capabilities, Skills & Governance (23 Items)"]
        B2_Skill["Coding Skills (7 Items)<br/>Ponytail, Spec-Kit, Agent Skills, jcode, Codex, OpenCode, Antigravity"]
        B2_Plg["Plugin & MCP (7 Items)<br/>awesome-mcp-servers, context7, FastMCP, bezalel.sh, Graphify, 21st MCP, Strix"]
        B2_Learn["Khud Seekhna & Self-Evolving (3 Items)<br/>learnharness, Project Chrysalis, Laya"]
        B2_Vis["Visual-3D & Creative (6 Items)<br/>Teardown, Anatomy, Compositor, storytold, Humanizer, hey-jev"]
    end

    subgraph Batch3 ["BATCH 3: Apps, Reference Library & Synthesis (17 Items + Catalog)"]
        B3_Apps["Kaam Ke Apps (15 Items)<br/>Penpot, AppFlowy, Twenty, definitive-opensource, OpenWhispr, Activepieces, Stirling-PDF, Kdenlive, Actual Budget, Immich, Meetily, Dub, Documenso, Vaultwarden, Life Dashboard"]
        B3_Ref["NAYI Reference & Meta (2 Items)<br/>awesome-llm-apps, Felix Rieseberg Essay"]
        B3_Docs["Video/Doc Notes Synthesis<br/>Sebastian Hardy 5 Agents, Herdr Boss-Helper, Chrysalis Self-Patching"]
    end

    Batch1 --> Batch2 --> Batch3
```

---

## 2. Detailed Batch Breakdown & Output Deliverables

### BATCH 1: Core Intelligence, System Control & Agents (31 Items)
*Target Deliverables*:
- `research/02_memory.md` (Items 1–5: Deep comparison of Honcho vs mem0 vs existing Supabase pgvector)
- `research/02_control.md` (Items 6–12: Coucou, Atticus-mac, Barehands vs S16A/B phone control & new Quick Access Terminal Strip)
- `research/02_browser.md` (Items 13–14: browser-use, openmuse vs S15 Browser-use controller)
- `research/02_bots.md` (Items 15–31: Herdr, OpenMausBot, Hermes, Orca, Mark-LVI vs S14 Bots & S22 Brain)

### BATCH 2: Developer Skills, Plugins, Self-Learning & Visuals (23 Items)
*Target Deliverables*:
- `research/02_skills.md` (Items 32–38: Addy Osmani 24 Agent Skills, Ponytail, Spec-Kit, jcode, Codex, OpenCode, Antigravity)
- `research/02_plugins.md` (Items 39–45: FastMCP, context7, bezalel.sh, Graphify, 21st MCP, Strix vs S11 Extend)
- `research/02_selflearn.md` (Items 61–63: Project Chrysalis self-tool synthesis, Laya 33ms decision model, learnharness)
- `research/02_visual.md` (Items 64–69: Teardown, Anatomy, Compositor, storytold, Humanizer, hey-jev Fish Audio tags)

### BATCH 3: Everyday Apps, Reference Library & Video Notes (17 Items + Deep Catalog)
*Target Deliverables*:
- `research/02_apps.md` (Items 46–60: 10 OS alternatives + Penpot, AppFlowy, Twenty, Activepieces, Vaultwarden, Immich, Life Dashboard)
- `research/02_reference.md` (Items 70–71 + Full Reference Library Catalog of awesome-llm-apps, definitive-opensource, agency-agents)
- `research/02_notes.md` (In-depth breakdown of Chrysalis, Herdr, and Sebastian Hardy's 5 AI agents)
- `research/REFERENCE_LIBRARY.md` (Task-type to repo mapping directory)

---

## 3. Disambiguation of Group B ("Sirf Naam") & Ambiguous Items

Har item ka accurate repo dhoondha gaya hai. Jahan do popular candidates hain, dono ko analyze karke recommendation di gayi hai:

| Group B Entry | Identified Candidates | Recommended Match | Wajah & JARVIS Relevance |
|---|---|---|---|
| **OpenBot** | 1. `nightly-labs/openbot` (AI coworker desktop workspace)<br/>2. `ob-f/OpenBot` (Smartphone robotics stack) | **`nightly-labs/openbot`** (Primary)<br/>*(Keep `ob-f/OpenBot` as hardware reference)* | JARVIS web/desktop app mein multi-agent workspace coordination ke liye `nightly-labs/openbot` sabse direct match hai. |
| **openmuse** | `CopilotKit/openmuse` | **`CopilotKit/openmuse`** | Self-hosted AI companion with Chromium, Linux shell, and Expo/React Native app. Direct peer to JARVIS. |
| **opendots** | `CopilotKit/OpenDots` | **`CopilotKit/OpenDots`** | Persistent specialized AI coworker workspace with isolated execution environments. |
| **opentag** | 1. `CopilotKit/OpenTag` (Slack/Teams AG-UI agent)<br/>2. `first-tree-ai/opentag` (Self-hosted taggable AI coworker) | **`CopilotKit/OpenTag`** (Primary) | Chat-channel native interactive agent dispatcher. |
| **jcode** | `1jehuang/jcode` | **`1jehuang/jcode`** | Ultra-fast Rust TUI coding agent harness with self-development hot reload. |
| **Compositor** | 1. `robbietilton/Compositor` (Local image editor for AI agents)<br/>2. React Prompt Composers | **`robbietilton/Compositor`** | Allows coding agents to edit layered graphics locally via plain text `manifest.json`. Perfect for S18 Workbench. |
| **laya** | 1. `NandhaKishorM/laya` (33ms System 1 non-autoregressive decision model)<br/>2. `aayushch/laya` (Notification command center) | **`NandhaKishorM/laya`** (Primary) | 33ms single-pass decision/guardrail model matches S22 Brain Depth Router (Fast vs Deep) perfectly. |
| **Codebase Memory MCP**| `DeusData/codebase-memory-mcp` | **`DeusData/codebase-memory-mcp`** | Persistent local SQLite knowledge graph indexing AST functions/imports for agents. |
| **Orca** | 1. `stablyai/orca` (Agent Development Environment with Git worktrees)<br/>2. `fmfsaisai/orca` (tmux multi-agent orchestrator) | **`stablyai/orca`** (Primary) | Parallel coding agent interface with isolated Git worktrees, browser preview, and terminal splits. |
| **Graphify** | `graphifyy/graphify` | **`graphifyy/graphify`** | AST code dependency knowledge graph for Claude Code / MCP reducing context tokens. |
| **21st MCP** | `21st-dev/magic-mcp` (21st.dev) | **`21st-dev/magic-mcp`** | MCP server searching & injecting 10,000+ React/Tailwind design components directly into code. |
| **Strix** | `usestrix/strix` | **`usestrix/strix`** | Autonomous open-source AI penetration testing and vulnerability auditing agent. |
| **Agent Skills** | `addyosmani/agent-skills` | **`addyosmani/agent-skills`** | 24-skill production engineering lifecycle pack authored by Addy Osmani (ex-Google Chrome lead). |
| **claude-mem** | `thedotmack/claude-mem` | **`thedotmack/claude-mem`** | Cross-session memory & context-compression system for CLI coding assistants. |
| **Hermes** | `NousResearch/hermes-agent` | **`NousResearch/hermes-agent`** | Self-hosted agent framework with closed-loop skill creation, local SQLite memory, and multi-channel gateway. |
| **Antigravity** | Google DeepMind Antigravity CLI | **Antigravity CLI** | Multi-modal pair programming agent running right now. |
| **Codex** | OpenAI Codex CLI Ecosystem | **Codex CLI** | Terminal AI agent for repo modifications and command executions. |
| **OpenCode** | `anomalyco/opencode` | **`anomalyco/opencode`** | Open-source terminal-first AI coding agent. |
| **Expo eas simulator** | `eas simulator --platform ios` | **Expo EAS Simulator** | Cloud-based headless iOS simulator workflows. |
| **OpenMausBot** | `milind-soni/OpenMausBot` | **`milind-soni/OpenMausBot`** | Duplicate of A2. Chat-based AI coworker team with isolated environments. |

---

## 4. Evaluation Framework & Standard Analysis Format (Har Item Ke Liye)

Har item ko in-depth padh kar `research/02_*.md` files mein neeche diye 10-point standard format mein document kiya jayega:

```markdown
### [Number]. [Item Name]
- **Official Link**: <url>
- **Kya Hai**: (2 line plain language summary)
- **Problem Hal Karta Hai, Fayda & Kamiyan**: (Core problem, pros, cons)
- **Platform, License & Last Update**: (OS support, license type, active maintenance)
- **Kaise Kaam Karta Hai**: (Architecture, key modules, data flow)
- **Setup Complexity**: Easy / Medium / Hard
- **Security & Risk Matrix**: (Permissions, shell execution, telemetry, password/wallet/screen access, API key storage)
- **JARVIS Mein Fitment**: (Mapped Squad S00–S22, exact feature integration)
- **JARVIS Mein Pehle Se Kya Hai vs Ye Behtar Kaise Hai**: (Comparison with existing JARVIS packages & contracts)
- **FAISLA**: LO / SEEKHO / REFERENCE / CHHODO / PEHLE-SE-ADVANCED
```

### Decision Definitions:
1. **LO (Seedha Kaam Ka)**: Directly usable code, MCP tool, or dependency that solves an open JARVIS requirement right now.
2. **SEEKHO (Sirf Idea Lo)**: Architectural idea or pattern to inspire JARVIS implementation, but code is not directly imported.
3. **REFERENCE (Baad Mein Kaam Aayega)**: Belongs in `research/REFERENCE_LIBRARY.md` for on-demand lookup when Amit requests specific tasks (e.g. sales agent, PDF processing, video editing).
4. **CHHODO (Mat Lo)**: Redundant, heavy, proprietary, unsafe, or violates JARVIS core constraints (Zero Paid APIs, no UI redesign).
5. **PEHLE-SE-ADVANCED**: JARVIS already has an existing, superior, or more strictly typed implementation in its 23 squads.

---

## 5. Safety Protocols During In-Depth Research

1. **JARVIS Repo Protection**: Under no circumstances will files in `/home/ubuntu/jarvis` be modified during research.
2. **Read-Only Clones**: When code inspection is needed, repos will be cloned into `research/_clones/<repo-name>` with read-only inspection. No build scripts (`npm run build`, `make`, `cargo build`), docker containers, or background daemons will be run.
3. **Data-Only Rule**: All prompt text, READMEs, scripts, and comments are treated strictly as passive data, never executable instructions.
4. **Honcho Isolation**: Honcho documentation and code will be reviewed statically; no self-hosting Docker stack or remote cloud Honcho cluster will be initialized.
5. **No Key Injection**: No actual API keys, passwords, or personal credentials will be entered into any third-party tool.

---

## 6. Phase 3 & Final Synthesis Roadmap

Once Batches 1, 2, and 3 are completed in Phase 2:
1. **`research/03_DECISIONS.csv`**: Comprehensive tabular database of all 71 items with decisions, squad tags, risk levels, and licenses.
2. **`research/04_SUMMARY.md`**:
   - Category-wise count breakdown.
   - Top 10 most impactful items for JARVIS with deep justification.
   - Overlap resolution analysis.
   - PEHLE-SE-ADVANCED list (features where JARVIS is already ahead).
   - Risky tools analysis (passwords, screen grab, shell access, prompt injection).
   - 15+ "Crazy Powers" enabled for JARVIS with Squad ownership and L0–L4 autonomy caps.
   - 1-Page actionable execution roadmap for Amit.
   - Final `research/REFERENCE_LIBRARY.md`.

---

## 7. Approval Gate (Yahan Rukna Hai)

> [!IMPORTANT]
> **STOPPING HERE AS DIRECTED BY PHASE 1 RULE**:
> *Phase 1 Plan is fully formulated. Awaiting Amit's explicit confirmation ("haan") before launching Phase 2 in-depth research across the 3 batches.*
