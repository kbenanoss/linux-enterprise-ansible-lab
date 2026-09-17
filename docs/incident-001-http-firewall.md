# Incident 001 HTTP Service Unreachable

## Environment

- Control node: control
- Affected server: linux02
- Management address: 192.168.56.22
- Operating system: CentOS Stream 9
- Web server: Nginx
- Firewall: firewalld
- Configuration management: Ansible

## Incident summary

Remote clients could not access the Nginx website on linux02. The server remained reachable through ICMP and SSH.

## Reported symptom

An HTTP request from the control node to linux02 timed out or failed:

```bash
curl --connect-timeout 3 -I http://192.168.56.22
