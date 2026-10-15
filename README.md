# Lynis Custom Security Tests

**Author:** Vasu Jindal

This project contains custom shell tests developed for Lynis, an open-source Linux security auditing tool.

## Tests Included

### 1. CUST-1010 — Systemd Service Risk Analyzer
Checks selected systemd service unit files and executable permissions for potential security risks. It also checks selected hardening settings for locally configured root services.

### 2. CUST-1020 — Scheduled Task Risk Analyzer
Checks selected cron directories for unsafe file permissions, ownership issues, and directory permissions.

## Environment
- Ubuntu 20.04.6 LTS
- Lynis 2.6.2
- Shell scripting

## How to Run

Place the custom test file in the Lynis include directory, then run:

```bash
sudo lynis audit system
```

Check shell syntax with:

```bash
sudo sh -n /usr/share/lynis/include/tests_custom
```

**Note:** These are custom Lynis shell tests, not standalone Nmap NSE scripts. Review and test them in a safe environment before using them on production systems.
