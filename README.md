# Enterprise Linux Ansible Lab

This project demonstrates administration and automation of a multi-server CentOS Stream 9 environment using Vagrant, VirtualBox and Ansible.

## Architecture

| Host | Address | Purpose |
|---|---|---|
| control | 192.168.56.20 | Ansible control node |
| linux01 | 192.168.56.21 | Managed Nginx server |
| linux02 | 192.168.56.22 | Managed Nginx server |

## Implemented capabilities

- SSH key-based administration
- Dedicated operations administrator
- Passwordless automation through controlled sudo configuration
- Package management
- Chrony time synchronization
- Nginx installation and service management
- Jinja2 server-specific templates
- firewalld configuration
- SELinux-enforcing operation
- HTTP health validation
- Configuration-drift remediation
- Idempotent Ansible execution

## Project structure

```text
.
├── ansible.cfg
├── inventory
│   ├── hosts.ini
│   └── group_vars
│       └── all.yml
├── playbooks
│   ├── baseline.yml
│   └── webserver.yml
├── templates
│   └── index.html.j2
├── docs
│   └── incident-001-http-firewall.md
├── requirements.yml
└── roles
