# Incident Response (Alert → Resolution)

**Flow:** Alert intake → Triage (0–5m) → Stabilize (5–15m) → RCA → Postmortem

### Roles
- **Incident Commander (IC):** owns timeline & comms.
- **Comms Lead:** updates Slack `#status` and stakeholders.
- **Ops Lead:** runs fixes; delegates to SMEs.
- **Scribe:** captures timeline and artifacts.

### First 5 Minutes (Triage)
- Acknowledge alert; open **SEV** using the matrix.
- Declare IC; start timeline in the ticket.
- Snapshot: users affected, blast radius, first failure time.
- Safeguards: feature flags/rollback, traffic throttle, read-only mode.

### Stabilize (5–15 Minutes)
- Pick the fastest path to user impact reduction.
- Run **health checks**:
  - API/DB latency & error rate
  - Auth failures/spikes
  - Queue backlogs / disk / CPU / TLS expiries
- Document every change (who/what/when).

### Communication Cadence
- SEV1: every 15 min; SEV2: every 30–45 min.
- Message format: *Impact → Action → ETA → Next update*.

### Resolution & Closure
- Verify recovery on dashboards and logs.
- Document final state, user comms, and follow-ups.
- Schedule **RCA** within 3 business days.

**See also:**
- `severity_matrix.md`
- `runbook_checklist.md`
- `rca_template.md`
