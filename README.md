# Sysco Dynamic Architecture AI Map (DAAIM) — Interactive Demo Package

Self-contained, 100% offline interactive demo of **DAAIM** aligned to the GCP architecture design (Cloud Run + Cloud Pub/Sub + AlloyDB/Cloud SQL `pgvector` + Vertex AI RAG/MCP).

## Quick Start (No Server or Internet Required)

1. Unzip `sysco-daaim-demo.zip`.
2. Double-click **`index.html`** to open it in Chrome, Edge, Firefox, or Safari.
3. All CSS/JS dependencies (`assets/tailwindcss.min.js`) are bundled locally — works completely offline behind corporate firewalls.

*(Optional)* If you prefer serving it locally over HTTP:
```bash
python3 -m http.server 8080
```
Then open `http://localhost:8080`.

## Package Contents

- `index.html` — Full interactive DAAIM web prototype (Light & Dark mode toggle included).
- `assets/tailwindcss.min.js` — Local offline Tailwind runtime (zero external CDN requests).
- `docs/daaim_architecture_design_doc.md` — Detailed GCP Architecture & System Design Document with Mermaid diagrams.
- `docs/daaim_ui_reference.png` — Target DAAIM UI mockup reference.

## Suggested Stakeholder Demo Walkthrough

1. **Interactive Topology (`Map View`):** Click any CI node (`Order Service`, `Redis Cache`, `Storage Account`), drag nodes to rearrange, toggle layouts (`Layered`, `Blast Radius`, `Compact Grid`), filter by `Highlight: Gaps Only`, or export SVG/JSON.
2. **AI-Inferred Dependency Review:** Click the dashed green arrow (`VM-ORD-DB-01 → Storage Account`) to inspect Gemini's extracted evidence and test **Confirm as Valid** or **Dismiss**.
3. **Simulated GCP Ingestion Pipeline:** Click **Simulate Pub/Sub + AI Sync** in the top header to animate the 4-stage ServiceNow → Confluence/SharePoint → Vertex AI + MCP → Map update flow.
4. **Live RAG + MCP Assistant:** Click **Ask DAAIM Agent** (or the **Faster Issue Resolution** card) and try the built-in prompts for blast radius, DR/Cyber gaps, or live ServiceNow incident checks.
5. **Governance & Portfolio Views:** Switch between `Order Service`, `WMS Core Logistics`, and `Payment Gateway`, and walk through **Missing Info & Gaps** (with Resolve / 90d Waiver actions), **Documentation** (with RAG chunk previews), **Insights**, and **Connectors & Policy**.
