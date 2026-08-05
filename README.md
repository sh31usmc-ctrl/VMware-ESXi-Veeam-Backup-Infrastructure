# VMware ESXi & Veeam Backup Infrastructure

## Overview
This project demonstrates the setup of a bare-metal VMware ESXi hypervisor environment integrated with Network Attached Storage (NAS) and automated disaster recovery workflows using Veeam Backup & Replication.

## Architecture & Hardware Specs
- **Hypervisor:** VMware ESXi host configured with static networking and storage datastores.
- **Storage Target:** Buffalo LinkStation NAS providing network storage shares and backup targets.
- **Management:** VMware vCenter Server / ESXi Web Console.
- **Backup Suite:** Veeam Backup & Replication (Veeam Agent integration for VM workloads).

---

## Technical Implementations
- **Hypervisor Setup & Optimization:**
  - Configured bare-metal ESXi host, including static IP assignment, custom DNS settings, and NTP synchronization.
  - Implemented Physical-to-Virtual (P2V) machine migrations using `Disk2Vhd`.
  - Configured Virtual Switch (vSwitch) topologies and optimized network interface card (NIC) metric priorities.
- **Storage & Datastore Management:**
  - Provisioned and mounted HDD/SSD datastores to ESXi for virtual disk allocation.
  - Configured Buffalo LinkStation NAS for user/group access permissions and network file sharing protocols.
- **Backup & Business Continuity (BCDR):**
  - Configured Veeam Backup & Replication agents across host virtual machines.
  - Executed full system bare-metal backups, incremental backups, and VM snapshot policies.
  - Tested disaster recovery scenarios including full VM restores and file-level recovery from Veeam backup sets.
