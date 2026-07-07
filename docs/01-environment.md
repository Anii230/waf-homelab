# Environment

This document describes the infrastructure used to build the WAF Homelab. It serves as a baseline reference before deploying any applications or security components.

## Host Machine

- OS: CachyOS
- CPU: Intel Core i5-9300HF
- RAM: 16 GB
- Hypervisor: KVM/QEMU

## Target VM

| Component | Specification |
|----------|---------------|
| Operating System | Ubuntu Server 26.04 LTS |
| Firmware | UEFI |
| vCPUs | 2 |
| Memory | 4 GB |
| Storage | 40 GB QCOW2 (Thin Provisioned) |
| Network | NAT (virbr0) |
| Remote Access | OpenSSH |

## Why Ubuntu Server?

Ubuntu Server was selected because it provides a lightweight environment without a graphical interface, closely resembling how Linux servers are deployed in production. Since this project focuses on infrastructure, networking, and web security, using a server edition allows direct interaction with the operating system through the command line while minimizing unnecessary resource usage.

## Why CLI?

The objective of this project is to build practical Linux administration skills alongside understanding Web Application Firewalls.

Using the command line helps develop familiarity with common administrative tasks such as:

- Package management
- Service management
- Docker administration
- Log analysis
- Network troubleshooting
- SSH-based remote administration

These are the same workflows commonly used when managing Linux servers in professional environments.

