# Awesome-Managed-Cloud-Network-Firewall

# Top Managed Cloud Network Firewall Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Cloud-Native Firewalls, Self-Hosted NGFW & Open-Source Security Platforms*  
**Last updated: October 2026**

This repository tracks notable **commercial managed cloud firewall platforms** and **open-source projects** that protect cloud workloads, VPCs, and hybrid networks — from fully managed cloud-native firewalls to self-hosted next-generation firewall distributions and eBPF-based packet filtering engines.

**Examples** include AWS Network Firewall, Azure Firewall, Google Cloud Cloud Armor, Palo Alto VM-Series Cloud, Fortinet FortiGate-VM, Check Point CloudGuard, Cisco Secure Firewall, Cloudflare Magic Firewall, Sophos Cloud Firewall, and SonicWall NSv (the category leaders).

**Open-source emphasis**: Managed cloud network firewall is a strong open-source domain. **OPNsense** and **pfSense** lead as the most widely deployed open-source firewall distributions, with **IPFire** providing a simpler, security-focused alternative. **fos1** brings Kubernetes-native firewall distribution on Talos Linux, **neuwerk** delivers cloud-native eBPF egress firewalling, and **Polycube** provides eBPF/XDP-based packet filtering with hash-table rule lookup for superior latency and throughput . **BunkerWeb** and **morfic** round out the ecosystem with Web Application Firewall and Kubernetes-native control plane capabilities . This section is heavily expanded.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[AWS Network Firewall](https://aws.amazon.com/network-firewall/)**  
  **AWS's managed network firewall** — VPC-level protection with stateful and stateless rule groups, Suricata-compatible IPS, and deep packet inspection . **Centralized deployment across VPCs via Transit Gateway** . **Best for AWS-native network security** .

- **[Azure Firewall](https://azure.microsoft.com/en-us/products/azure-firewall/)**  
  **Microsoft's cloud-native firewall** — stateful inspection with FQDN filtering, threat intelligence, and Azure Monitor integration . **Azure Firewall Premium** adds TLS inspection and IDPS . **Best for Azure-native network security** .

- **[Google Cloud Cloud Armor](https://cloud.google.com/armor)**  
  **Google's DDoS and WAF protection** — Layer 7 filtering with preconfigured WAF rules, rate limiting, and adaptive protection . **Best for GCP-native application protection** .

- **[Palo Alto VM-Series Cloud](https://www.paloaltonetworks.com/)**  
  **Virtual next-generation firewall** — App-ID, User-ID, and Content-ID with cloud-native scaling . **Best for Palo Alto-centric organizations** .

- **[Fortinet FortiGate-VM](https://www.fortinet.com/)**  
  **Virtual NGFW** — consolidated security with FortiOS and cloud integration . **Best for Fortinet ecosystem users** .

- **[Check Point CloudGuard](https://www.checkpoint.com/)**  
  **Cloud network security** — unified management with threat prevention . **Best for Check Point users** .

- **[Cisco Secure Firewall](https://www.cisco.com/)**  
  **Enterprise firewall with cloud deployment** — integrated with Cisco Security Cloud Control . **Best for Cisco-centric organizations** .

- **[Cloudflare Magic Firewall](https://www.cloudflare.com/)**  
  **Cloud edge firewall** — network-level filtering at Cloudflare's global edge . **Best for Cloudflare ecosystem users** .

- **[Sophos Cloud Firewall](https://www.sophos.com/)**  
  **Cloud-managed firewall** — synchronized security with Sophos Central . **Best for Sophos ecosystem** .

- **[SonicWall NSv](https://www.sonicwall.com/)**  
  **Virtual firewall** — NSv series for cloud and virtualized environments . **Best for SonicWall users** .

## Open-Source GitHub Projects

### Firewall Distributions

- **[OPNsense](https://github.com/opnsense/core)**  
  **The leading modern open-source firewall distribution**, BSD-2-Clause licensed with **5,000+ GitHub stars** . **FreeBSD-based with clean UI and regular six-month release cycles**  . **Integrates Suricata for inline intrusion detection**  . **ZFS boot environments for safe rollback** and **API-based automation**  . **Full firewall suite with VPN (WireGuard, OpenVPN, IPsec), traffic shaping, and NetFlow**  . **The modern alternative to pfSense with faster development pace** . **Best for cloud VMs and enterprise deployments** .

- **[pfSense](https://github.com/pfsense/pfsense)**  
  **The most widely deployed open-source firewall**, Apache-2.0 licensed with **3,000+ GitHub stars** . **FreeBSD-based with web GUI and stateful packet inspection**  . **Supports Snort and Suricata for IDS/IPS, IPsec, OpenVPN, and WireGuard**  . **Extremely mature with the largest community and extensive documentation**  . **pfSense Plus is closed source; CE receives features with delay**  . **Best for established deployments with predictable behavior** .

- **[IPFire](https://github.com/ipfire/ipfire-2.x)**  
  **Security-focused open-source firewall**, GPL-3.0 licensed . **Linux-based with color-coded zones (Green/Red/Blue/Orange)** for network segmentation  . **Lighter than pfSense and OPNsense, easier to harden**  . **Strong track record on security patch delivery** . **Built-in Pakfire package manager and QoS support**  . **Best for smaller teams and environments where simplicity matters** .

### Cloud-Native Firewalls

- **[neuwerk](https://github.com/moolen/neuwerk)**  
  **Cloud-native eBPF network egress firewall**, MIT licensed . **Runs as central infrastructure on the network level** — no application changes required  . **Dynamic, DNS-based firewall for allow/deny egress traffic**  . **Raft-based cluster with NATS JetStream** for distributed state management  . **TLS bootstrap ceremony with leader election** . **Supports glob hostnames, CIDR allowlist, and audit mode**  . **Best for cloud-native egress control** .

- **[fos1](https://github.com/GizmoTickler/fos1)**  
  **Kubernetes-based router/firewall distribution on Talos Linux**, MIT licensed . **Immutable OS with Kubernetes orchestration and declarative infrastructure-as-code**  . **Full routing, NAT, DNS, DHCP, NTP, WireGuard, IDS, and DPI paths implemented** as of April 2026  . **eBPF-based packet processing with stateful filtering**  . **IDS/IPS via Suricata and network protocol analysis via Zeek**  . **Best for Kubernetes-native firewall deployments** .

- **[morfic](https://github.com/fire833/morfic)**  
  **Kubernetes-native firewall/routing control plane**, open-source  . **User/kernel space network control plane** . **Best for Kubernetes network control** .

### eBPF & XDP Packet Filtering

- **[Polycube](https://github.com/polycube-network/polycube)**  
  **eBPF and XDP-based framework for network services**, Apache-2.0 licensed . **Provides tools for creating firewalls, bridges, and routers**  . **pcn-iptables** — drop-in iptables replacement using eBPF with hash-table rule lookup for stable latency and throughput as rules scale  . **Supports egress, stateful filtering, and full IPv4/IPv6 L4 protocol coverage**  . **Outperforms traditional iptables with large rulesets when implemented efficiently**  . **Best for high-performance packet filtering** .

- **[xdp-filter](https://github.com/xdp-project/xdp-tools)**  
  **XDP-based packet filtering from XDP project**, open-source . **Hash-table rule lookup with stable latency** — unlike XDP-Firewall's linear search  . **Supports TCP and UDP on both IPv4 and IPv6**  . **Best for stateless high-throughput filtering** .

### Web Application Firewalls

- **[BunkerWeb](https://github.com/bunkerity/bunkerweb)**  
  **Cloud-native Web Application Firewall (WAF)**, AGPL-3.0 licensed with **8,000+ GitHub stars** . **NGINX-based with ModSecurity integration**  . **Multisite mode protects multiple applications from a single instance**  . **Autoconf for Docker and Kubernetes** — automatically reconfigures based on container labels or Ingress resources  . **Supports SQLite, MariaDB, MySQL, and PostgreSQL** for state storage  . **Best for web application protection in cloud-native environments** .

- **[ModSecurity](https://github.com/owasp-modsecurity/ModSecurity)**  
  **The most widely deployed open-source WAF engine**, Apache-2.0 licensed . **Runs as a module for Apache, Nginx, and IIS** — supports OWASP Core Rule Set (CRS) . **Best for traditional WAF deployments** .

- **[OWASP Coraza](https://github.com/corazawaf/coraza)**  
  **Modern open-source WAF written in Go**, Apache-2.0 licensed . **100% compatible with OWASP CRS v4** — 20-40% higher throughput than ModSecurity . **Best for Kubernetes/Envoy environments** .

### Additional Strong Open-Source Options

- **Untangle** — Linux-based NGFW with IDPS focus  .
- **Smoothwall** — NAT mapping, IDPS, and multi-WAN support  .
- **Zenarmor** — OPNsense plugin with DPI, application control, and TLS inspection  .
- **VyOS** — Linux-based router/firewall OS with VLANs and VPN support  .
- **OpenWrt** — Linux-based router OS with firewall capabilities  .
- **metal-stack firewall-controller** — Kubernetes controller for bare-metal firewalls with nftables and Suricata  .
- **cloud-snitch** — AWS activity map visualization and firewall inspired by Little Snitch  .

**Frameworks for building custom cloud network firewall solutions**: Combine **OPNsense** or **pfSense** for proven firewall distributions deployable on cloud VMs . Use **neuwerk** for cloud-native eBPF egress firewalling with DNS-based policies  . Deploy **fos1** for Kubernetes-native firewall on Talos Linux with full routing and IDS/IPS  . Choose **Polycube** for high-performance eBPF packet filtering with hash-table rule lookup  . Integrate **BunkerWeb** for Web Application Firewall protection in cloud-native environments  . Use **ModSecurity** or **Coraza** for traditional WAF deployments . Note that true managed cloud firewalls with global infrastructure, automatic scaling, and vendor-supported SLAs (AWS Network Firewall, Azure Firewall, Palo Alto VM-Series) remain primarily commercial territory; open-source stacks provide strong firewall distributions, eBPF filtering, and WAF foundations that require integration for complete cloud network security.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud network firewalls handle critical network traffic and security policies. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations.
- **Patch cadence is a security control** — unpatched firewall firmware is a high-value attack surface. Prefer platforms with active maintenance (OPNsense, pfSense, IPFire) over abandoned ones  .
- **eBPF firewalls are not inherently superior** — their effectiveness depends on implementation. Hash-table rule lookup (Polycube pcn-iptables, xdp-filter) maintains stable latency as rules scale, while linear search (XDP-Firewall) degrades significantly  .
- **Management interface exposure is a common misconfiguration** — never expose the firewall admin UI directly to the internet. Use VPN or bastion hosts for administrative access  .
- **License considerations**: OPNsense uses BSD-2-Clause, pfSense uses Apache-2.0 (Plus is closed source), IPFire uses GPL-3.0, neuwerk uses MIT, and Polycube uses Apache-2.0. Verify licensing against your use case before committing .
- The open-source ecosystem provides strong firewall distributions, eBPF filtering, and WAF foundations, but **global infrastructure, automatic scaling, and vendor-supported SLAs** remain primarily commercial offerings.

---

**Made for network engineers, cloud architects, and organizations seeking cloud firewall sovereignty.**
Let's make managed cloud network firewalls more open, transparent, and secure.
