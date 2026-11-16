# Ada Research Agent — Frontend Studio

This is the Next.js web application for Ada Research Agent, providing an interactive research studio, live execution tracking, document vault management, and report exploration.

## Overview

- **Framework**: Next.js 16 (App Router) with React 19 and TypeScript
- **Styling**: Tailwind CSS v4 with custom dark editorial design system
- **State & Communication**: React Context, SSE (Server-Sent Events) for real-time run progress, custom React hooks
- **Markdown & Citations**: `react-markdown` with GFM, interactive citation drawer, and evidence score panels

## Key Pages & Routes

- `/` — Landing page and introduction to Ada Deep Research
- `/studio` — Research launchpad for querying, track configuration, vault selection, and preflight checks
- `/run/[id]` — Live research progress feed, real-time stage progression, event logs, and source inspector
- `/report/[id]` — Rendered research monograph with interactive citation inspection, evidence scores, and follow-up queries
- `/vault` — Document library with multi-format upload (PDF, DOCX, CSV, TXT), paste memo, preview, and reindexing
- `/dashboard` — System statistics, run history summary, and quick access to research assets
- `/history` — Searchable chronological archive of previous research runs and reports
- `/architecture` — Interactive system architecture visualization and pipeline data flow
- `/settings` — User preferences, account management, and password update

## Development & Build Commands

```bash
# Install dependencies
npm ci

# Start local development server (http://localhost:3000)
npm run dev

# Run ESLint validation
npm run lint

# Type-check TypeScript code
npx tsc --noEmit

# Production build
npm run build

# Start production server
npm run start
```

## Environment Configuration

The frontend connects to the FastAPI backend API via `NEXT_PUBLIC_API_URL`:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```
