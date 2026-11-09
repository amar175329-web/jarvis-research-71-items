# JARVIS Reference Library — Master Catalog
**Document**: `research/REFERENCE_LIBRARY.md`  
**Purpose**: On-demand repository and knowledge index for JARVIS when Amit assigns specific tasks.  
**Rule**: Check the license column before copying any code. If the license is restrictive or commercial, the rule is *"Sirf padhke seekho"* (architectural pattern only). If permissive (MIT/Apache-2.0/BSD), code adaptation is permitted.

---

## 1. Quick Task-to-Repo Routing Matrix

| When Amit says... | Look up this Repo / Tool | What to learn or take | License | Action Advice |
|---|---|---|---|---|
| *"Ek naya RAG app ya document QA pipeline banao"* | `Shubhamsaboo/awesome-llm-apps` | Production chunking recipes, hybrid search, citations | Apache-2.0 | Code adapt karo; local Ollama/Supabase par mount karo. |
| *"Multi-agent coding session chalao bina file overwrite kiye"* | `stablyai/orca` & `1jehuang/jcode` | Isolated Git worktrees, TUI multiplexing, split panes | MIT | Worktree spawning script directly use karo. |
| *"Outbound sales ya lead enrichment agent setup karo"* | `ethanplusai/sellbird` | Website buying signal extraction, local SQLite loop | MIT | Code adapt karo; email sending ko L2 confirmation par lock karo. |
| *"Kisi paid software ka open-source replacement dhoondho"* | `mustbeperfect/definitive-opensource` | Comprehensive verified FOSS alternatives catalog | MIT | Catalog lookup karo. |
| *"Naya MCP tool banao Python mein"* | `PrefectHQ/fastmcp` | Fast `@mcp.tool` decorator framework, stdio transport | Apache-2.0 | Directly use as builder library. |
| *"Bade codebase ki call graph aur dependencies samjhao"* | `graphifyy/graphify` & `DeusData/codebase-memory-mcp` | Tree-sitter AST parsing, SQLite symbol table | MIT | Local binary tool run karke AST inspect karo. |
| *"Design-Clone ya Web UI ke liye modern components inject karo"*| `21st-dev/magic-mcp` | 10,000+ React/Tailwind/Framer Motion UI components | MIT | Direct component code inject karo. |
| *"Supabase RLS policies aur API endpoints ko pentest karo"* | `usestrix/strix` | Dynamic security auditing, exploit proof-of-concept | AGPL-3.0 | Sandboxed Kali Docker mein chalao; external scan strictly forbidden. |
| *"Naye bot ke liye deep domain system prompt likho"* | `msitarzewski/agency-agents` | 230+ battle-tested persona briefs across domains | MIT | Prompt text copy karke customize karo. |
| *"Machine ya engine ka 3D exploded view aur video banao"* | `elvarofficial/teardown` | Three.js mechanical disassembly, procedural MP4 recording | MIT | Ready-to-run Claude Code skill. |
| *"Software backend architecture ko isometric machine mein badlo"*| `wheresryan22/anatomy` | Interactive SVG/WebGL mechanical brass-and-glass models | MIT | Ready-to-run visualization skill. |
| *"Fish Audio voice mein natural emotion (hansi, aah) dalo"* | `henryklunaris/hey-jev` | Fish Audio S2.1 emotion tags (`[chuckling]`, `[sighing]`) | MIT | Prompt string mein emotion tags inject karo. |
| *"Private self-hosted password aur API key vault setup karo"* | `dani-garcia/vaultwarden` | Lightweight Rust Bitwarden server (<30MB RAM) | AGPL-3.0 | Docker container run karo; L2 approval enforce karo. |
| *"PDFs ko merge, OCR, redact ya split karo bina cloud bheje"*| `Stirling-Tools/Stirling-PDF` | 100% local PDF manipulation REST endpoints | GPL-3.0 | Connect via local REST API; do not modify core code. |
| *"Agent ko naya tool synthesize karne do safely"* | `GoogleCloudPlatform/generative-ai` (Chrysalis) | Shapley score critique, OPA sandbox, human sign-off gate | Apache-2.0 | Architecture pattern replicate karo; enforce L2 gate. |
| *"Agent routing latency ko 33ms tak fast karo"* | `NandhaKishorM/laya` | Non-autoregressive System 1 single-tensor decision model | MIT / ONNX | Local ONNX runtime mount karo. |
| *"Recurring multi-app automation flow setup karo"* | `activepieces/activepieces` | 200+ TypeScript pieces, webhooks, crons | MIT | S12 automation engine ke roop mein use karo (sirf "har baar" kehne par). |
| *"YouTube ke liye video assemble karo script se"* | `kdenlive.org` (Kdenlive / MLT) | Programmatic MLT XML video timeline rendering | GPL-3.0 | Scripted XML render engine reference. |
| *"High-res photos aur phone media auto-backup karo"* | `immich-app/immich` | Local facial clustering, timeline backup, mobile app | AGPL-3.0 | Standalone self-hosted server reference. |
| *"Personal budget track karo bina bank data share kiye"* | `actualbudget/actual` | Local-first encrypted SQLite envelope budget | MIT | Standalone finance reference. |
| *"Branded short links aur QR codes create karo"* | `dubinc/dub` | Modern link shortener, geo-analytics, Next.js app | AGPL-3.0 | Marketing & YouTube channel link shortener. |
| *"Client contracts aur agreements digitally sign karwao"* | `documenso/documenso` | Cryptographic digital signature infrastructure | AGPL-3.0 | Design-Clone SaaS client onboarding reference. |
| *"Meeting audio transcribe karke action items nikalo"* | `Meetily` | Local Whisper transcription, automated task extraction | MIT | S09/S08 meeting note intake pattern. |
| *"Desktop GUI app ko agent CLI mein convert karo"* | `HKUDS/CLI-Anything` (clianything.cc) | 7-phase GUI to JSON CLI converter pipeline | MIT | Directly wrap desktop software with structured JSON outputs. |
| *"Android phone par apps automate karo (WhatsApp, Maps, Settings)"* | `google/artemis` | 99%+ AndroidWorld benchmark, Flash/Pro loops, Logcat capture | Apache-2.0 | S16A phone execution engine ke roop mein mount karo. |
| *"Bina paid API ke kisi website ka direct typed client banao"* | `kalil0321/reverse-api-engineer` | HAR network capture, TypeScript/Python API synthesis | MIT | Network endpoints sniff karke clean client code generate karo. |

---

## 2. Exhaustive Directory of Core Reference Repositories

### Group 1: awesome-llm-apps (100+ Production Recipes)
- **Repo**: `Shubhamsaboo/awesome-llm-apps` | **License**: Apache-2.0 | **Advice**: Code lene ki poori chhoot hai.
- **Key Sub-Pipelines for JARVIS**:
  1. *RAG & Document Intelligence*: Advanced chunking, re-ranking with Cohere/BGE, multi-modal PDF parsing, tabular data QA.
  2. *Autonomous Agents*: Multi-agent research swarms, financial market analyst agents, automated bug squashers.
  3. *Voice & Audio Agents*: Real-time audio streaming, speech-to-speech agents, local Whisper integrations.
  4. *Memory Implementations*: Graph memory, vector hybrid search, conversation buffer windows.

### Group 2: definitive-opensource (Production FOSS Alternatives)
- **Repo**: `mustbeperfect/definitive-opensource` | **License**: MIT | **Advice**: Tool discovery ke liye reference lookup.
- **Top Replacements for Amit's Ecosystem**:
  1. *Storage & Drive*: Nextcloud / Seafile (replaces Google Drive / Dropbox).
  2. *Notes & Docs*: AppFlowy / Logseq (replaces Notion / Obsidian Sync).
  3. *Analytics*: Umami / Plausible (replaces Google Analytics with zero cookies).
  4. *Project Management*: Penpot / Taiga / Vikunja (replaces Jira / Asana / Figma).
  5. *Media & Entertainment*: Jellyfin (replaces Plex / Netflix).

### Group 3: awesome-mcp-servers (500+ Model Context Protocol Tools)
- **Repo**: `punkpeye/awesome-mcp-servers` | **License**: CC0 Public Domain | **Advice**: Read-only directory.
- **Key Categories to Call On-Demand**:
  1. *Database Tools*: Postgres MCP, SQLite MCP, Supabase MCP, Redis MCP.
  2. *Developer Tools*: Git MCP, GitHub MCP, Docker MCP, Sentry MCP.
  3. *Filesystem & Search*: Brave Search MCP, Fetch MCP, Local Filesystem MCP.
  4. *Productivity*: Google Workspace MCP, Slack MCP, Notion MCP.

### Group 4: agency-agents (230+ Specialist AI Agents)
- **Repo**: `msitarzewski/agency-agents` | **License**: MIT | **Advice**: Copy-paste system prompts as templates.
- **Top Personas for JARVIS Bots Workspace**:
  1. *Technical Lead*: Enforces clean architecture, code reviews, and test requirements.
  2. *Security Auditor*: Proactively challenges authentication, RLS, and data validation boundaries.
  3. *Growth & Copywriting Specialist*: Drafts high-converting landing page copy and social hooks.
  4. *DevOps & SRE Engineer*: Monitors CI/CD pipelines, Docker health, and error logging.
