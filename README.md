# Ansible Control Node – Hardened SSH & Remote Access Automation

This project configures a Fedora Linux system as an **Ansible control node** with:
- Hardened SSH key-based remote access
- Tailscale mesh VPN for zero-config connectivity
- Ansible automation for user security & system lockdown

## ⚔️ Phase 1: Remote SSH Access via Tailscale

✔️ Password login disabled  
✔️ Custom SSH port (`2222`)  
✔️ Key-based access only  
✔️ Multi-device remote control (MacBook, iPhone)

### 🔧 Tools Used
- Tailscale (mesh VPN)
- SSH key authentication (ED25519)
- macOS Terminal + Fedora

### 🔐 Security Enhancements
- Root login disabled
- `fail2ban` active with log sync to MacBook
- SSH logs mirrored nightly

---

## ⚙️ Phase 2: Ansible Automation for Secure Access

Using a self-written playbook:

- 👤 Created a hardened user: `sysops`
- 🔑 Installed MacBook's public SSH key
- 🔒 Applied SSH hardening via `sshd_config`
- 🔁 Restarted SSH safely with `systemctl`

### 📁 Playbook File
[`playbooks/secure-access.yml`](playbooks/secure-access.yml)

---

## 🧠 Why This Matters

✅ Designed for DevSecOps, remote sysadmin, and infrastructure automation  
✅ Push-button onboarding for new secure users  
✅ Config replicable across air-gapped or cloud-hosted servers

---

## 🛰️ Live Devices in the Mesh

- **MacBook Pro** (client)
- **Fedora Laptop** (control node)
- **iPhone via Termius** (client with SSH auth)

All connected over Tailscale. All login-secured via public key only.

---

## 🚀 Next Phase

Coming up:  
- Multi-node Ansible roles  
- Full infrastructure-as-code for user creation, backups, firewall, and alerts  
- Auto-push to GitHub via cron + bash

> _Built by [Carlos Semeao](https://www.linkedin.com/in/carlos-semeao-04938a357/) • Linux + DevSecOps Apprentice_
