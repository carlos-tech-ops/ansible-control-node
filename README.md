# 🛡️ Ansible Control Node – Hardened SSH & Remote Access Automation

This project transforms a **Fedora Linux laptop** into a hardened Ansible control node, featuring:

- 🔐 SSH key-only remote access  
- 🌐 Tailscale mesh VPN for secure zero-config connectivity  
- ⚙️ Automated system lockdown via Ansible playbooks

---

## ⚔️ Phase 1: Remote SSH Access via Tailscale

✔️ Password login disabled  
✔️ Custom SSH port (`2222`)  
✔️ Key-based access only (ED25519)  
✔️ Multi-device control (MacBook, iPhone via Termius)  

**Security Enhancements:**
- Root login disabled  
- `fail2ban` active and logs synced nightly to MacBook  
- SSH logs mirrored for auditing

---

## 🔧 Tools Used

- **Tailscale** – private mesh VPN  
- **OpenSSH (ED25519)** – hardened key authentication  
- **macOS Terminal + Fedora Workstation** – dev and control environment  

---

## ⚙️ Phase 2: Ansible Automation for Secure Access

**Playbook File:** `playbooks/secure-access.yml`

This playbook automates:
- 👤 Creation of a secure user: `sysops`  
- 🔑 SSH key setup for MacBook login  
- 🔒 SSH daemon hardening (`sshd_config`)  
- 🧯 Safe restart of SSH service using `systemctl`  
- 📂 Backup of original SSH configuration

---

## 🧠 Why This Project Matters

✅ Built for real-world DevSecOps, remote sysadmin, and infrastructure-as-code workflows  
✅ Push-button onboarding for secure users  
✅ Easily replicable across air-gapped systems, cloud instances, and physical machines  

---

## 🛰️ Live Devices in the Mesh (via Tailscale)

- **MacBook** (admin terminal)  
- **Fedora Laptop** (Ansible control node)  
- **iPhone via Termius** (remote client w/ key authentication)  

All devices communicate securely over Tailscale and authenticate via public SSH key only.

---

## 🚀 Next Phase (Planned)

Coming soon:

- 🧩 Multi-node Ansible role-based deployment  
- 🔄 Git auto-push of state/config logs via `cron + bash`  
- 🔐 Infrastructure-as-code: secure users, backups, firewall, fail2ban alerts  
- 📡 Extend to VPS, Raspberry Pi, or cloud VMs

---

🧑‍💻 Built by **Carlos Semeao**  
📍 Based in Luton, UK  
🎯 Linux + DevSecOps Apprentice | GitHub: [carlos-tech-ops](https://github.com/carlos-tech-ops)  
⏱️ Last updated: 2025-05-30
