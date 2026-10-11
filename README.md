# SOC Investigation Labs

Hands-on Security Operations Center (SOC) investigation labs built to practice alert triage, endpoint telemetry analysis, evidence collection, and incident documentation.

> **Scope:** Defensive security and SOC Analyst Level 1 workflows. All tests are performed in a personal lab environment.

## Lab Environment

- **SIEM / security monitoring:** Wazuh 4.14.8
- **Endpoint:** Windows 11
- **Monitoring server:** Ubuntu 24.04.4 LTS running in VMware
- **Endpoint agent:** Wazuh Agent 4.14.8
- **Endpoint agent name:** `WINDOWS-ENDPOINT`

## Investigations

| Case | Scenario | Status | Main Skills |
|---|---|---|---|
| [01 — Windows Failed Logon Detection](cases/01-windows-failed-logon/README.md) | Review Windows Security Event ID 4625 and the corresponding Wazuh alert | Evidence collected; cause not confirmed | Windows Event Logs, Wazuh alert triage, evidence-based assessment |
| 02 — File Integrity Monitoring (FIM) | Detect and investigate a test-file change | Planned | File integrity monitoring, baseline vs. change analysis |
| 03 — PowerShell Activity Review | Inspect collected PowerShell telemetry and identify visibility gaps | Planned | Endpoint telemetry, process/activity analysis |
| 04 — Alert Triage and Correlation | Correlate related events and determine escalation priority | Planned | Event correlation, prioritization, escalation |

## Investigation Workflow

1. **Prepare** — define a safe, controlled test and expected evidence.
2. **Generate** — perform the test on the lab endpoint.
3. **Collect** — inspect the relevant Windows event and Wazuh event/alert.
4. **Analyze** — separate observed facts from assumptions; correlate timestamps and fields.
5. **Decide** — document triage outcome and recommended next actions.
6. **Report** — record evidence, limitations, and lessons learned.

## Repository Structure

```text
soc-investigation-labs/
├── README.md
├── cases/
│   └── 01-windows-failed-logon/
│       └── README.md
├── evidence/
│   └── README.md
├── templates/
│   └── incident-report-template.md
└── scripts/
    └── README.md
```

## Evidence and Safety

- Reports distinguish confirmed observations from hypotheses.
- No real credentials, tokens, personal data, or production logs should be committed.
- Screenshots should be sanitized before publishing.
- Planned cases are labeled as planned; they are not represented as completed work.

## Current Learning Goals

- Investigate Windows authentication events.
- Verify that endpoint events reach the SIEM.
- Interpret Wazuh rule IDs and alert levels in context.
- Correlate events and avoid premature conclusions.
- Produce concise, reproducible SOC L1 investigation reports.

## Disclaimer

This repository documents learning exercises in a personal lab. It is not a claim of professional SOC employment or production incident-response experience.
