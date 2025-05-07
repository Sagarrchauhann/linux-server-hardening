# linux-server-hardening

This project focuses on hardening a Linux server and analyzing its security using the [Lynis](https://cisofy.com/lynis/) auditing tool.

##  Objective

To implement key security practices on a Linux server and evaluate their effectiveness using before-and-after security scans.

---

##  Contents

- `Linux Server Hardening and Security Analysis.docx` – Detailed report on steps taken and their impacts
- `lynis-before.txt` – Lynis scan output before applying hardening measures
- `lynis-after.txt` – Lynis scan output after applying hardening
- `README.md` – This file

---

## Hardening Steps Taken

### SSH Configuration
- Disabled root login
- Changed default SSH port
- Disabled empty passwords

### Firewall (UFW)
- Enabled UFW
- Allowed only required ports (HTTP, HTTPS, custom SSH)

### Audit and Logging
- Enabled auditd for activity tracking
- Configured rsyslog for enhanced logging

### Filesystem Security
- Applied `nosuid`, `nodev`, and `noexec` mount options to `/tmp`, `/var/tmp`

### System Updates
- Applied system and kernel updates
- Enabled automatic security updates

### User & Group Management
- Removed unused users/groups
- Enforced strong password policies

---

## Lynis Scan Results

| Metric       | Before | After  |
|--------------|--------|--------|
| Lynis Score  | 61     | 70     |

###  Remaining Suggestions
- Install AIDE or Tripwire for file integrity
- Disable core dumps
- Enable AppArmor or SELinux
- Review root crontab entries

---

## Conclusion

A +9 point improvement in the Lynis score reflects effective implementation of hardening techniques. This setup provides a stronger security posture, better logging, and reduced attack surface.

## Full Documentation

You can view the full detailed documentation in [Developing a Secure File Transfer System Using SFTP on a Linux Server.docx]

---
