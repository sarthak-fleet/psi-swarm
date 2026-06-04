# Project Status

Last updated: 2026-06-04

## Current Scope

psi-swarm is a local-first helper for fleet and web-performance work. It measures Web Vitals across repeated Lighthouse runs and realistic device/network presets so users can reason about p50, p75, p90, and p99 instead of trusting one noisy PageSpeed/Lighthouse result.

## Done

- Node CLI supports `run`, `discover`, `serve`, `history`, and `compare` workflows.
- Headless Chrome and Lighthouse runs produce percentile tables, LCP element identification, ranked opportunities, and static HTML reports.
- Local browser UI exists as an Astro + React + Tailwind controller for the CLI `serve` agent.
- Compute stays local; the browser UI talks to the local agent through CORS/SSE.
- Local SQLite history supports tagged runs and before/after comparisons.
- Optional reasoning can use local-ai or an OpenAI-compatible backend.
- Claude/Codex usage paths are documented through the installable skill and AGENTS guidance notes.

## Planned Next

1. Keep Node 22 LTS as the supported path until the Lighthouse 12 / Node 24 trace-mark issue is resolved.
2. Improve the local web controller so users can run, compare, and inspect swarms without dropping to the CLI.
3. Add clearer fleet/demo examples that compare real product pages before and after performance work.
4. Decide whether psi-swarm should stay a fleet helper or gain a hosted report/gallery surface.

## Deferred / Parked

- Hosted RUM or real-user p99 collection is deferred; psi-swarm is lab data, not a RUM replacement.
- Cloud execution is parked because compute is intentionally local for now.
- Paid monitoring, team accounts, and alerting are deferred behind a stronger local workflow.
