# RCA – INC-1234 (Redacted)
Summary: Elevated auth failures in US-West (45m). Root cause: expired OAuth secret on a background worker.
Impact: ~12% login failures; no data exposure.
Actions: rotate secret; add secret-expiry alert; run chaos test monthly.
