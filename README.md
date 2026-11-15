# Awesome-Enterprise-Cloud-Security-Compliance

## Top Enterprise Cloud Security & Compliance Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on CSPM, CNAPP, Runtime Protection & Self-Hosted Security Scanners*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Cloud Security & Compliance**. These tools help organizations continuously monitor cloud configurations, detect misconfigurations, protect workloads at runtime, and maintain compliance across multi-cloud environments—covering everything from native CSPM services to agentless CNAPP platforms and command-line open-source scanners.

**Examples** include Wiz, Orca Security, Palo Alto Prisma Cloud, Microsoft Defender for Cloud, AWS Security Hub, Google Security Command Center, Lacework FortiCNAPP, Prowler, and Trivy (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted cloud security posture management, open-source vulnerability scanning, and community-driven runtime protection—ideal for organizations seeking data sovereignty and avoiding per-vCPU or per-resource pricing that compounds at scale. The open-source landscape is genuinely functional: **Prowler** provides a multi-cloud CSPM scanner with 500+ checks under Apache 2.0 , **Trivy** covers container and IaC vulnerability scanning , and **Falco** delivers eBPF-based runtime threat detection .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The enterprise cloud security market is estimated at approximately $40 billion to $45 billion in 2026, with the high-growth CNAPP sub-segment surpassing $12.5 billion at a >20% CAGR. The sector has transitioned from a highly fragmented landscape of disconnected point tools into a heavily concentrated market dominated by major cloud hyperscalers and top platform vendors through aggressive suite consolidation and multi-billion-dollar acquisitions.

## SaaS/Hosted Platforms

| Product | Company Size / Valuation | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|--------------------------|-------------|-------------------|--------------------------|
| **[Microsoft Defender for Cloud](https://azure.microsoft.com/en-us/products/defender-for-cloud/)** | ~$3.89 Trillion (Market Cap) | **Widest hybrid and multicloud coverage** (Azure, AWS, GCP, and on-premises via Azure Arc) with a functional free foundational CSPM layer. **Trade-off**: per-resource pricing can spike in elastic environments; advanced features reserved for paid Azure customers . | **Foundational CSPM**: $0 (Included); **Defender CSPM**: ~$5.11/billable resource/month; **Defender for Servers**: ~$4.91/server/month (Plan 1) | **Free forever**: Foundational CSPM (secure score, continuous assessment, basic recommendations). **Free trial**: 30-day free trial per Azure plan/resource type (1 trial per AWS account/GCP project); excludes storage malware scanning. |
| **[Google Security Command Center](https://cloud.google.com/security-command-center)** | ~$3.60 Trillion (Alphabet Market Cap) | **Best for Kubernetes-heavy GCP workloads**—specialized detection per workload type (events, containers, VMs) in Premium. Standard tier is genuinely useful and free. **Trade-off**: multicloud coverage nearly nonexistent; price jump from Standard to Premium can surprise teams . | **Standard Tier**: $0 (Free); **Premium (Pay-As-You-Go)**: Starts at $0.0071/vCPU-hour for Compute Engine / Cloud Run; **Premium Subscription**: ~5% of annualized GCP spend (min. ~$15,000/yr) | **Free forever (Standard tier)**: Continuous asset discovery, basic security health analytics, and vulnerability finding exports (subject to 500 MB/day findings upload cap and 1,000 req/min API quota). |
| **[AWS Security Hub](https://aws.amazon.com/security-hub/)** | ~$2.88 Trillion (Amazon Market Cap) | **Natural choice for AWS-heavy footprints**—deep integration with GuardDuty, Inspector, and Config. **Trade-off**: **no free tier**, multicloud coverage limited to Azure, and cost can scale unpredictably with finding volume . | **Security Checks (CSPM)**: $0.0010 per security check (first 100,000 checks/account/region/month; Config recorded separately); **Finding Ingestion**: $0.00003 per event beyond free limit | **Free forever**: First 10,000 finding ingestion events/account/region/month (findings from native checks always free). **Free trial**: 30-day free trial per account across all regions for Security Hub Essentials checks. |
| **[Palo Alto Prisma Cloud](https://www.paloaltonetworks.com/prisma/cloud)** | ~$263 Billion (Market Cap) | **Broadest toolset on paper** with mature compliance content and custom policy support. **Trade-off**: operational weight—agents on everything, long rollout, and four acquired products duct-taped together meaning multiple consoles and policy engines. Small teams feel that hardest . | Enterprise credit-based licensing starting at **~$30,000/year** (purchased in blocks of 100 Prisma Cloud Credits; consumption scaled by workload/container/identity volume) | **No perpetual free tier**. **Free trial**: 30-day free trial / guided Proof of Concept (PoC) scoped to specific cloud accounts and core CNAPP capabilities (CSPM/CWP). |
| **[CrowdStrike Falcon Cloud Security](https://www.crowdstrike.com/)** | ~$234 Billion (Market Cap) | Cloud workload protection extending Falcon's endpoint detection to cloud compute, containers, and Kubernetes. | Annual enterprise contract based on workload/node volume (Flex License starts at **~$233.99** per workload/seat for 3-yr terms via enterprise distribution) | **No perpetual free tier**. **Free trial**: 15-day free trial of the CrowdStrike Falcon platform with access to activate Falcon Cloud Security modules; extendable via sales. |
| **[Lacework FortiCNAPP](https://www.lacework.com/)** | ~$90 Billion (Fortinet Market Cap; acquired for $152.3M) | **Mature behavioral detection via Polygraph** and native integration with the Fortinet portfolio. **Trade-off**: lower G2 rating (4.4/5) than competitors; hybrid agent/agentless model can confuse teams expecting a clear choice; **Lacework's valuation collapsed from $8.3B to $152.3M** before Fortinet acquisition . | AWS Marketplace minimum starting tier: **$25,000/12 months** (Standard tier capped at 500 vCPUs; Pro capped at 334 vCPUs; Enterprise capped at 250 vCPUs) | **No perpetual free tier**. **Free trial**: 30-day negotiated Proof of Value (PoV) evaluation granted via Fortinet sales/marketplace with predefined test criteria. |
| **[Datadog Cloud Security](https://www.datadoghq.com/)** | ~$65 Billion (Market Cap) | Security monitoring integrated into Datadog's observability platform—CSM Pro, CWS, and Cloud SIEM. | **CSM Pro**: **$10/host/month** billed annually ($12/host on-demand month-to-month; requires base Infrastructure tier at $15/host/month); **CWS**: **$15/host/month** ($180/host/year) | **Free forever (Core platform)**: Free tier capped at 5 hosts (1-day metric retention). **Free trial**: 14-day full-access free trial for Datadog Cloud Security Management (CSM/CWS) across connected hosts and cloud accounts. |
| **[Wiz](https://www.wiz.io/)** | $32 Billion (Acquisition by Alphabet) | **Agentless CNAPP with the cleanest UI and fastest setup in the category.** Security graph prioritizes misconfigurations into attack paths. **Trade-off**: runtime protection is still thin, and it is **SaaS-only**—regulated or EU shops needing self-hosted hit a wall . | Workload-based annual enterprise license starting at **~$24,000/year** (typically covering ~100 workloads across CSPM/vulnerability scanning modules) | **No perpetual free tier**. **Free trial**: 14 to 30 days guided Proof of Concept (PoC) scoped to specific cloud accounts/workloads with full code-to-cloud graph scanning. |
| **[Orca Security](https://orca.security/)** | ~$1.8 Billion (Private Valuation) | **Agentless side-scanning for fast, wide coverage from day one.** Reachability filtering shrinks CVE noise instead of just re-sorting it. **Trade-off**: smaller brand than Wiz—you sometimes have to sell it internally; UI is fine, not the prettiest . | AWS Marketplace listed entry plan starting at **$124,440/year** for Small-Medium enterprise tier; custom private offers scaled by average concurrent compute workloads | **No perpetual free tier**. **Free trial**: 30-day cloud risk assessment / Proof of Concept trial provisioned via AWS Marketplace or direct sales. |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Prowler](https://github.com/prowler-cloud/prowler)** | [![Stars](https://img.shields.io/github/stars/prowler-cloud/prowler?style=social&color=white)](https://github.com/prowler-cloud/prowler/stargazers) | **The leading open-source CSPM scanner for multi-cloud environments.** Apache 2.0 licensed, **500+ checks** covering AWS, Azure, GCP, Kubernetes, M365, GitHub, and more. Maps to **CIS, NIST, PCI-DSS, GDPR, HIPAA, SOC 2, and ISO 27001**. Runs with a single command (`pip install prowler && prowler aws`). CLI, dashboard, and optional local server. **Best for teams wanting a free, auditable CSPM baseline across multiple providers** without per-resource fees . |
| **[Trivy](https://github.com/aquasecurity/trivy)** | [![Stars](https://img.shields.io/github/stars/aquasecurity/trivy?style=social&color=white)](https://github.com/aquasecurity/trivy/stargazers) | **The most widely adopted open-source vulnerability scanner for containers, Kubernetes, code, and cloud.** Detects vulnerabilities, misconfigurations, secrets, and licenses. Apache 2.0. **Best for shift-left security**—scan container images before deploy and catch CVEs early . |
| **[Falco](https://github.com/falcosecurity/falco)** | [![Stars](https://img.shields.io/github/stars/falcosecurity/falco?style=social&color=white)](https://github.com/falcosecurity/falco/stargazers) | **CNCF runtime security for Kubernetes and containers.** eBPF-based detection of suspicious network connections, file writes, and process executions. **<1% CPU overhead** for most workloads. Detected a malicious postinstall script's network request in **400ms** in a real-world supply chain test . **Best for catching zero-day exploits that bypass static scanners**—68% of supply chain attacks that caused data leaks bypassed static SCA tools . |
| **[Scout Suite](https://github.com/nccgroup/ScoutSuite)** | [![Stars](https://img.shields.io/github/stars/nccgroup/ScoutSuite?style=social&color=white)](https://github.com/nccgroup/ScoutSuite/stargazers) | **Open-source multi-cloud security auditing tool.** CLI with HTML report covering AWS, Azure, and GCP. **Best for quick security assessments** without a full CSPM platform—generates readable reports for audit or initial posture review . |
| **[CloudSploit](https://github.com/aquasecurity/cloudsploit)** | [![Stars](https://img.shields.io/github/stars/aquasecurity/cloudsploit?style=social&color=white)](https://github.com/aquasecurity/cloudsploit/stargazers) | Open-source cloud security scanning for AWS, Azure, GCP, Oracle, and GitHub. Detects misconfigurations and compliance risks. **Best as a lightweight CSPM alternative** for organizations already using Aqua's ecosystem . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[OpenClarity](https://github.com/openclarity/openclarity)** | [![Stars](https://img.shields.io/github/stars/openclarity/openclarity?style=social&color=white)](https://github.com/openclarity/openclarity/stargazers) | **Open-source tool for security and observability of cloud-native applications.** CNCF-related project (1,351 stars, actively updated). **Best for teams wanting broader cloud-native security visibility** beyond pure CSPM . |
| **[Kube-bench](https://github.com/aquasecurity/kube-bench)** | [![Stars](https://img.shields.io/github/stars/aquasecurity/kube-bench?style=social&color=white)](https://github.com/aquasecurity/kube-bench/stargazers) | Checks Kubernetes clusters against **CIS Kubernetes Benchmark**. Lightweight Go binary. **Best for Kubernetes compliance validation** as part of a broader security program . |

**Frameworks for building custom systems**: Choose **Prowler** for multi-cloud CSPM scanning with 500+ compliance-mapped checks , **Trivy** for container and IaC vulnerability scanning , and **Falco** for eBPF-based runtime threat detection —creating a free, self-hosted security stack that covers posture, vulnerabilities, and runtime without per-vCPU licensing.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud security platforms require broad read access to cloud APIs and workload metadata; enforce least-privilege IAM roles and audit data access.
- **Pricing models vary dramatically and hidden costs compound.** **Lacework's $25,000/12-month AWS Marketplace floor** has a perverse structure: the vCPU cap **shrinks** as tiers rise (Standard 500, Pro 334, Enterprise 250)—so Enterprise on a 500-vCPU fleet requires **two packs, doubling the annual line** . **AWS Security Hub has no free tier** and costs scale unpredictably with finding volume . **Wiz is SaaS-only**—regulated or EU shops needing self-hosted cannot use it . **Open-source tools are genuinely viable but require assembly**: Prowler covers CSPM across clouds , Trivy handles vulnerabilities , and Falco catches runtime threats that bypass static scanners . **Validate multi-cloud coverage, runtime detection depth, and total cost of ownership** before committing.

---

**Made for cloud security engineers, SOC analysts, and organizations building multi-cloud defense.**  
Let's make enterprise cloud security more open, observable, and cost-predictable.
