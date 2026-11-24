# Dynamic Architecture AI Map (DAAIM) — Interactive Concept Demo

A self-contained, offline-ready interactive prototype illustrating how an enterprise can unify CMDB topology (e.g., ServiceNow), distributed documentation (Confluence & SharePoint), and Cloud AI (GCP Pub/Sub + AlloyDB/Cloud SQL `pgvector` + Vertex AI RAG/MCP) into a single living architecture map with automated compliance gap detection.

> **Note:** All application names, CI identifiers, IP addresses, incidents, people, and documents in this demo are 100% synthetic sample data for concept demonstration purposes.

## Quick Start (No Server or Internet Required)

1. Unzip `daaim-public-demo.zip`.
2. Double-click **`index.html`** to open it directly in Chrome, Edge, Firefox, or Safari.
3. All assets (`assets/tailwindcss.min.js`) are bundled locally — zero external CDN dependencies.

*(Optional)* Serve locally over HTTP:
```bash
python3 -m http.server 8080
```
Then open `http://localhost:8080`.

## Package Contents

- `index.html` — Interactive DAAIM web prototype (includes Light & Dark mode toggle).
- `assets/tailwindcss.min.js` — Local offline Tailwind runtime.
- `docs/daaim_architecture_design_doc.md` — Reference GCP architecture and system design document with Mermaid diagrams.

## Demo Walkthrough

1. **Interactive Topology (`Map View`):** Click any node (`Order Service`, `Redis Cache`, `Storage Account`), drag nodes around, switch layouts (`Layered`, `Blast Radius`, `Compact Grid`), filter by `Highlight: Gaps Only`, or export the diagram as SVG/JSON.
2. **AI-Inferred Dependency Review:** Click the dashed green arrow (`VM-ORD-DB-01 → Storage Account`) to inspect the AI-extracted evidence and test **Confirm as Valid** or **Dismiss**.
3. **Simulated Event Pipeline:** Click **Simulate Pub/Sub + AI Sync** in the header to step through CMDB sync, documentation scraping, Vertex AI + MCP correlation, and live map updates.
4. **Live RAG + MCP Assistant:** Click **Ask DAAIM Agent** (or the **Faster Issue Resolution** card) and try the built-in prompts for blast radius, DR/Cyber gaps, or live incident checks.
5. **Governance & Portfolio Views:** Switch between `Order Service`, `Fulfillment Core`, and `Payment Gateway`, and explore **Missing Info & Gaps** (with Resolve / 90d Waiver actions), **Documentation** (with RAG chunk previews), **Insights**, and **Connectors & Policy**.
