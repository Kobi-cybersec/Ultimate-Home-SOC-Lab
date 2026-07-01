# My Enterprise Home SOC Lab Journey

Welcome to my cybersecurity portfolio. This repository documents the step-by-step engineering, deployment, and monitoring of an isolated Home Security Operations Center (SOC) lab environment built from the ground up.

---

## 🛠️ Phase 1: Physical Hypervisor Layer
* **Hardware Node:** Dedicated server platform equipped with processing cores, upgraded high-speed DDR5 RAM, and high-performance NVMe storage.
* **Hypervisor:** Proxmox VE (Virtual Environment).
* **Network Infrastructure:** Segmented layout using a custom subnet mask topology to handle local asset management.

### Key Hurdles Overcome:
* **The `Exit Code 100` Error:** Diagnosed a package manager failure during core updates. Successfully resolved it by disabling the restricted enterprise update streams and manually mapping the system to the community **No-Subscription** repository.

---

## 🖥️ Phase 2: Staging the Target Environment
* **Asset Name:** `linux-target-01`
* **Operating System:** Headless Ubuntu Server (Text-only command-line interface).
* **Resource Mapping:** 2 vCPU cores (Indexed as Core 0 and Core 1), 2GB RAM, 32GB NVMe Virtual Disk storage.

### Local Tooling Installed:
* **`htop`:** Deployed via CLI to monitor live system processes, track memory footprint, and observe background resource anomalies.
