# n8n-workflows.lumenosis.com

This repository powers [n8n-workflows.lumenosis.com](https://n8n-workflows.lumenosis.com), a searchable library of production-ready n8n templates.

It is built for one job: help people find, inspect, and reuse real workflows quickly.

## What This Is

- A hosted collection of **2,000+ n8n workflows** (current index snapshot: **2,055**)
- Structured by category, trigger type, complexity, and integrations
- Searchable by both metadata and workflow JSON-related content

## What People Can Do on the Site

- Search across **titles, descriptions, integrations, node count, and JSON content**
- Filter by:
  - Trigger (`Webhook`, `Scheduled`, `Manual`, `Complex`)
  - Complexity (`Low`, `Medium`, `High`)
  - Category
  - `Active only`
- Use quick category navigation to jump directly into a domain
- Open workflow details and review:
  - Status
  - Trigger
  - Complexity
  - Node count
  - Category
  - Integrations
- Take actions per workflow:
  - **Download JSON**
  - **View JSON**
  - **View Diagram**

## Search and Indexing (How It Works)

At a high level:

- `vercel_workflows.json` is the prebuilt index used by the frontend
- The index contains global stats plus per-workflow searchable fields
- The UI supports fast filtering/search and keeps state through URL params
- API routes provide workflow retrieval, search, and download operations

This is why users can search broad terms (for example tools, trigger types, node counts, and workflow-related JSON text) and still get useful matches.

## Current Indexed Snapshot

From the hosted index data:

- Total workflows: **2,055**
- Active workflows: **217**
- Inactive workflows: **1,838**
- Total nodes across workflows: **29,518**
- Unique integrations: **50**
- Index timestamp: **2025-08-21**

## Repository Structure

- `workflows/` - source workflow JSON files
- `api/workflows/` - API-served workflow files
- `vercel_workflows.json` - aggregated searchable index
- `api/` - API layer for search, details, and downloads
- `src/`, `static/` - frontend app and assets
- `build_vercel_data.py` - index generation utility

## Why This Exists

Most workflow libraries are hard to navigate once they get large.

This project keeps discovery simple at scale: search fast, inspect quickly, and export exactly what you need.
