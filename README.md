# Sysco Dynamic Architecture AI Map (DAAIM) — Interactive Demo v2

Self-contained, 100% offline interactive demo of **DAAIM** aligned to the GCP architecture design (Cloud Run + Cloud Pub/Sub + AlloyDB/Cloud SQL `pgvector` + **SAGE — Sysco Agentic AI Platform**).

## Quick Start (No Server or Internet Required)

1. Unzip this archive.
2. Double-click **`index.html`** to open in Chrome, Edge, Firefox, or Safari.
3. All dependencies (`assets/tailwindcss.min.js`) are bundled locally — works completely offline behind corporate firewalls, with a working **Dark Mode / Light Mode** toggle in the header.

## Highlights in v2

- **Executive Dashboard:** KPIs, Architecture Health meters, interactive Estate Domain Map, Top AI Recommendations, Risk Hotspots, Quick Ask SAGE box, and Report Export.
- **Business-User Navigation:** Grouped into Overview, Governance & Assurance, and Platform.
- **Human-in-the-Loop (HITL) Verification:** Amber `?` badges on nodes missing docs/owners, inline Inspector verification actions (Attach Doc / Assign Owner / Mark N/A / 90d Waiver), and centralized `Governance & HITL` queue with audit history.
- **Hosted On (Box Outline) Legend:** Color-coded 2.5px node outlines for **Equinix**, **Edge**, **AWS**, **Azure**, and **GCP**, with all hosting locations in **Europe (Amsterdam & Dublin)**.
- **Updated Connectors & Deep Links:** `Illumio / Tufin` (Network Flow Approval), `Infralens` (Infra Inventory), `Wiz & Brinqa` (Security), `ThreatModeler & Archer` (Cyber SRA), and `Datadog` (Monitoring); inspector deep links to ServiceNow CMDB, Infralens, and Datadog.
