# Awesome-Centralized-Data-Retention-Backup-Policies

## Top Centralized Data Retention & Backup Policies Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Policy-Driven Retention Management, Immutable Backup Governance & Compliance Automation*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Centralized Data Retention & Backup Policies**. These tools help organizations define, enforce, and audit retention rules across backup systems, SaaS applications, and cloud workloads—ensuring data is kept for exactly as long as compliance requires, protected against tampering, and disposed of securely when no longer needed.

**Examples** include Druva Policy Management, Microsoft Purview Retention, Symantec Enterprise Policy, Forcepoint DLP Policy, Netskope Policy Management, Zscaler Cloud Policy, HashiCorp Sentinel, Styra OPA, Cloudflare Zero Trust Policies, Palo Alto Panorama, and Cisco Secure Policy Engine (the category leaders).

**Open-source emphasis**: This section highlights every major active project for policy-as-code engines, backup retention automation, and compliance-driven data lifecycle management—ideal for platform engineers, compliance teams, and organizations seeking transparent, vendor-neutral policy enforcement without proprietary lock-in.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Druva Policy Management](https://www.druva.com/)**  
  Cloud data protection platform with centralized backup policy configuration covering backup frequency, retention periods (Daily, Weekly, Monthly, Yearly in GFS model), long-term retention tiering, and Data Lock immutability. Retention policies apply to all new and existing recovery points upon change, with separate settings for files and emails [citation:19][citation:25]. Management Console provides unified visibility across NAS shares, servers, and SaaS workloads [citation:1].

- **[Microsoft Purview Retention](https://www.microsoft.com/en-us/security/business/microsoft-purview)**  
  Information lifecycle management across Microsoft 365 services including Exchange, SharePoint, OneDrive, and Teams. Retention labels and policies define how long content is kept and when it's deleted, with in-place preservation that requires no separate backup process [citation:2][citation:26]. Microsoft 365 Backup service adds immutable recovery points for OneDrive, SharePoint, and Exchange with configurable recovery windows of 3 months to 2 years [citation:20].

- **[Symantec Enterprise Policy Management](https://www.broadcom.com/)**  
  Enterprise Console provides centralized policy management across Endpoint Security, Web Security, and Data Security scopes. Administrators manage device policies, cloud service subscriptions, and SCIM configurations from a single interface with audit event logging for compliance [citation:3].

- **[Forcepoint DLP Policy Engine](https://www.forcepoint.com/)**  
  Data Security Cloud | SSE provides DLP pattern management with predefined compliance libraries (HIPAA, SOX, PCI) and custom patterns supporting exact match, file fingerprinting, MIME type, and file size criteria. DLP policies control actions on protected applications based on pattern matches [citation:4].

- **[Netskope Policy Management](https://www.netskope.com/)**  
  DSPM Policy Management dashboard provides centralized visibility into active policies, severity-ranked alert volumes, and drill-down investigation. Policies can be edited, duplicated, archived, or status-toggled (enabled/disabled) from a unified interface [citation:5].

- **[Zscaler Cloud Policy](https://www.zscaler.com/)**  
  ZIA and ZPA policy engine with granular controls including GenAI prompt capture from Cloud Application Control policies, flexible URL filtering rule creation, and scheduled upgrade channel selection for Cloud Connectors. Policy enforcement extends to Zero Trust Branch for FedRAMP environments [citation:6].

- **[HashiCorp Sentinel](https://www.hashicorp.com/sentinel)**  
  Policy-as-code framework for Terraform Enterprise and HCP Terraform. Sentinel policy sets are organized by provider, target domain (security, networking), and environment, with version-controlled policy repositories and pipeline automation for testing against representative Terraform configurations [citation:7].

- **[Styra OPA (DAS)](https://www.styra.com/)**  
  Enterprise control plane for Open Policy Agent providing centralized policy lifecycle management across Kubernetes, Terraform, microservices, and gateways. Policies written in Rego define authorization and infrastructure guardrail requirements with least-privilege enforcement [citation:8].

- **[Cloudflare Zero Trust Policies](https://www.cloudflare.com/)**  
  Access and Gateway policies with configurable log retention periods varying by plan tier (24 hours for free Access logs, 180 days for Enterprise). Logpush enables export to R2 or external destinations, with Customer Metadata Boundary for geographic data localization [citation:9].

- **[Palo Alto Panorama](https://www.paloaltonetworks.com/)**  
  Centralized security policy management for VM-Series firewalls across NSX-T and other environments. Device Groups enable policy push to multiple firewalls, with dynamic address groups for workload-based rule targeting and zone/DoS protection profiles for layered defense [citation:10].

- **[Cisco Secure Policy Engine](https://www.cisco.com/)**  
  Common Policy framework with ISE as the context hub, sharing user and application context across ACI, SD-WAN, and firewalls. SGT (Security Group Tag) mappings enable consistent policy enforcement at different network domains—campus, data center, and cloud [citation:11].

## Open-Source GitHub Projects

- **[Backup Warden](https://github.com/backup-warden/backup-warden)**  
  Python-based backup retention policy engine supporting GFS-style rotation (minutely, hourly, daily, weekly, monthly, yearly) across filesystem paths. Configurable per-path retention rules with include/exclude pattern matching, S3 endpoint support, Slack webhook notifications, and Docker deployment [citation:12].

- **[3tears-backup](https://pypi.org/project/3tears-backup/)**  
  Encrypted database backup tool with built-in GFS retention (keep N daily/weekly/monthly, prune rest). Supports PostgreSQL and Yugabyte with storage-agnostic object store injection (S3, filesystem), client-side AES-256-GCM encryption, and restore verification into throwaway databases [citation:18].

- **[Plakar Policy](https://github.com/plakarkorp/plakar)**  
  Open-source backup tool with a dedicated `policy` command for managing retention policies. Policies define keep rules (e.g., `per-week=1 since='3 months'`) that drive `plakar prune` operations. Supports named policies with option-based configuration and YAML/JSON output [citation:28].

- **[BorgBackup Prune](https://github.com/borgbackup/borg)**  
  Mature open-source deduplicating backup tool with GFS retention via `borg prune`. Options include `--keep-daily`, `--keep-weekly`, `--keep-monthly`, `--keep-within` intervals, and prefix filtering for multi-dataset repositories. Checkpoint archives are automatically cleaned [citation:29].

- **[OSPAC (Open Source Policy as Code)](https://pypi.org/project/ospac/)**  
  Declarative policy engine for automated compliance evaluation, using YAML/JSON policy files versioned in Git. Supports SPDX license compatibility, obligation tracking, and organizational policy rules—extensible to data retention compliance scenarios [citation:13].

- **[retention (Go package)](https://pkg.go.dev/github.com/orneryd/nornicdb/pkg/retention)**  
  Go library implementing retention policy management with legal hold support. Policies define deletion schedules, with `IsUnderLegalHold` preventing data erasure during litigation. Includes GDPR Article 17 erasure request handling with 30-day deadline enforcement [citation:21].

### Additional Strong Open-Source Options

- **[Microsoft 365 DSC](https://github.com/microsoft/Microsoft365DSC)** — Open-source Desired State Configuration tool for extracting and managing Microsoft 365 tenant configuration, including retention and compliance settings, with drift detection [citation:2].
- **Plakar** — Full backup tool with policy management beyond just retention; the policy subcommand integrates with prune operations for automated lifecycle management [citation:28].
- **Community cron/script-based retention wrappers** — Many organizations build custom retention enforcement using `find -mtime` or similar primitives alongside backup tools.

**Frameworks for building custom systems**: Combine **BorgBackup** or **Plakar** for backup execution with GFS retention, **Backup Warden** for filesystem-based rotation policies, and **OSPAC** for policy-as-code compliance definitions—integrated via cron or CI pipelines for automated enforcement and audit logging.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Data retention policies must comply with applicable regulations (GDPR, HIPAA, SOX, industry-specific mandates) and organizational legal hold requirements; consult legal counsel before configuring deletion schedules.
- Self-hosted open-source retention tools require proper testing of restore procedures before relying on them for compliance; policy changes that reduce retention are destructive and should be reviewed.

---

**Made for compliance officers, backup administrators, platform engineers, and data governance teams.**  
Let's make data retention and backup policies more open, enforceable, and auditable.
