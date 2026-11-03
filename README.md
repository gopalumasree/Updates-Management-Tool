# VenuOps UMT — Agentless Windows Patching over RDP

**Patch Windows servers through existing RDP access—without WinRM or endpoint PowerShell. Manage Linux updates over SSH from the same portable Windows application.**

No permanent UMT endpoint agent. Scan, review, deploy, troubleshoot and report.

**[Product website & requirements](https://gopalumasree.github.io/Updates-Management-Tool/)** · **[Download Public edition](https://github.com/gopalumasree/Updates-Management-Tool/releases/latest)** · **[Visual PDF guide](https://github.com/gopalumasree/Updates-Management-Tool/releases/download/v0.8.2/UMT-0.8.2-Visual-Use-Guide.pdf)**

Created by **Venugopala Rao.P** · **+91 9908987878**

Part of **[VenuOps](https://github.com/gopalumasree/VenuOps)** — public infrastructure tools and guides.

## Download

**[Download the latest Public edition](https://github.com/gopalumasree/Updates-Management-Tool/releases/latest)**

Choose **UMT-0.8.2-Public-Protected-win-x64.zip** under **Assets**. Extract the entire ZIP into a writable folder and open **UpdatesManagementTool.exe**. Normal use does not require an owner passphrase.

The Word and PDF visual guides are included in `docs` and are also available as separate release downloads. The automatically generated **Source code** ZIP/tar.gz is this download-page repository, not the application.

## Windows patch management without WinRM

UMT uses an RDP session to start a temporary Windows Script Host worker and exchange results through an isolated redirected folder. The worker calls Windows Update APIs locally and uses the configured Windows Update/WSUS source. This path does not require enabling PowerShell remoting, remote WMI, Remote Registry or administrative SMB shares.

**Best fit:** administrators with approved RDP access who cannot readily introduce additional management protocols or permanent endpoint agents. RDP access, sufficient permissions, drive redirection and worker execution must be permitted. UMT does not bypass endpoint policy.

**Agentless means no permanent UMT endpoint agent, not zero endpoint execution.** The worker uses `cscript`, Windows Update APIs and local WMI checks. The tool PC uses a bundled PowerShell runtime; the Windows RDP worker does not require endpoint PowerShell.

## Troubleshoot and patch Windows and Linux devices

- Review exact patch plans before deployment, for a batch or one device.
- Inspect source/policy evidence, use applicable repairs and rescan the same device.
- Prepare a fresh Linux plan from verified working repositories when another source fails; exclusions and unknown totals remain visible.
- Retain groups, run history, HTML/Excel reports and optional schedules.
- Keep using the same extracted folder; use Backup / move and Restore when moving saved access.

## Quick start

1. **Servers & access:** add devices, check ports and enter access details.
2. **Patch options:** choose updates, exclusions and restart rules; start a scan.
3. **Review & patch:** review the exact plan, then apply it when ready.
4. **Activity & logs / Reports:** track results; troubleshoot and rescan individual devices.
5. **Groups & schedules:** save repeatable groups, configure schedules and filter historical reports.

Use **Scan only** first to validate access and results in your environment. Service scheduling is optional; portable manual use does not need a scheduling service.

## Current release: 0.8.2

- Operations, saved-access, service-repair and scan-input fixes.
- Windows and Linux troubleshooting with per-device follow-up actions.
- Review and deployment from verified working Linux sources when another source remains unresolved.
- Common batch patch review, groups, schedules and historical reports.
- Fix for concurrent report saves during parallel device work.
- Protected application files and a compact visual guide in Word and PDF.

## Validation and current limits

Automated regression, package integrity and native startup checks passed within the documented scope. Live deployment, installed-service lifecycle, logged-out scheduling and cross-PC credential migration acceptance remain pending. A broader saved-credential test process stopped before completion; the simulated scheduler tests passed separately.

Windows RDP/MFA work currently requires an unlocked portal session. Existing duplicate scheduler registrations are not automatically removed. Details are in the included `docs/VALIDATION.txt`.

Saved credentials are Windows/account-bound. Use the application's **Backup / move** and **Restore** workflow for migration, then validate access on the destination. Keep your operational data and recovery passphrase private.

## About this repository

This repository distributes **only the Public edition**, documentation and release notes. Application source, owner tools, signing keys, master archives, saved credentials, logs and reports are not published here.

The Public edition checks owner-signed application files for modification. This is application integrity protection, not a claim that local software cannot be reverse-engineered, and not Windows Authenticode signing.

Older downloads remain under **[Releases](https://github.com/gopalumasree/Updates-Management-Tool/releases)**. Each release includes a SHA-256 checksum for its Public ZIP.

## Report an issue

Use **[Issues](https://github.com/gopalumasree/Updates-Management-Tool/issues)** with the version, steps, expected result and actual result. Remove passwords, OTPs, keys, private server addresses and identifying operational data before sharing screenshots or logs.

Third-party notices are included with the application. Public download availability does not make the application source open source.
