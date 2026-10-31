# Release history

## 0.8.2 — Operations / ScanFix, Public Protected

### Included

- Saved-access, service-repair and scan-input fixes from the 0.8.2 Operations baseline.
- Per-device troubleshooting, rescan and patch review.
- Verified working-source Linux patch plans with unresolved sources shown separately.
- Batch review, groups, schedules and historical report filters.
- Synchronised diagnostic and repair updates during parallel report saves.
- Owner-signed application integrity checks and private-name obfuscation.
- Three-page visual use guide in Word and PDF.

### Validation

Automated regression, UI, integrity, archive and native startup checks passed within their stated scope. This packaging run did not deploy to live servers or install a scheduling service.

Live deployment, service lifecycle, logged-out scheduling and cross-PC credential acceptance remain pending. A broader saved-credential suite terminated early with exit `0x40000015`; the simulated scheduler suite passed separately. See the packaged validation document for details.

### Downloads

Use the Public Protected ZIP from the release assets. Owner/Master packages are not distributed here.
