# 🔒 Ansible Server Hardening

![Ansible](https://img.shields.io/badge/Ansible-Automation-EE0000?style=for-the-badge&logo=ansible)
![Security](https://img.shields.io/badge/Security-Hardening-green?style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-FCC624?style=for-the-badge&logo=linux)
![Vagrant](https://img.shields.io/badge/Vagrant-Local-1563FF?style=for-the-badge&logo=vagrant)

> Automated server security hardening using Ansible — implements CIS benchmark controls across SSH, firewall, kernel parameters, and system auditing.

## 🎯 What This Project Does

| Role | What it secures |
|------|----------------|
| 🔧 common | Package updates, removes insecure packages |
| 🔒 security | Kernel params, fail2ban, auditd, password policies |
| 🔑 ssh | SSH hardening, disable root login, max auth tries |
| 🛡️ firewall | UFW rules, deny all incoming except SSH/HTTP/HTTPS |

## 📁 Project Structure
ansible-server-hardening/
├── site.yml
├── inventory.ini
├── Vagrantfile
└── roles/
├── common/
├── security/
├── ssh/
└── firewall/

## ⚙️ Usage

```bash
# Clone and run
git clone https://github.com/pugal-123/ansible-server-hardening.git
cd ansible-server-hardening
vagrant up
```

## 🔒 Security Controls

### SSH
- ✅ Root login disabled
- ✅ Password authentication disabled
- ✅ Maximum 3 auth attempts
- ✅ Protocol 2 only

### Kernel
- ✅ IP forwarding disabled
- ✅ SYN flood protection
- ✅ ASLR enabled

### Firewall (UFW)
- ✅ Default deny all incoming
- ✅ Allow SSH, HTTP, HTTPS only

### System
- ✅ Fail2ban active
- ✅ Auditd monitoring
- ✅ Auto security updates
- ✅ Password expiry 90 days

## 👤 Author
**Pugazhenthi Muthu** — DevOps Engineer
github.com/pugal-123
