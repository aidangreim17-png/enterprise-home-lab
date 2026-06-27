# Enterprise Home Lab

> A virtualized enterprise IT environment built on Proxmox VE featuring Active Directory, Windows Server 2025, pfSense, Ubuntu Server, Docker, Group Policy, centralized software deployment, and enterprise file services.

---

## Overview

This project documents the design, deployment, and administration of a Windows enterprise home lab hosted on Proxmox VE. The lab simulates a small business environment by combining virtualization, networking, Linux services, Active Directory, Group Policy, centralized software deployment, and Windows administration.

The primary objective of this project is to gain hands-on experience with enterprise infrastructure while documenting implementation, troubleshooting, and administration procedures.

---

# Lab Architecture

```
                           Internet
                               │
                        Home Router
                               │
                        pfSense Firewall
                         192.168.50.1
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
        │                      │                      │
 Ubuntu Server             Windows Server        Windows 11
     Docker                  2025 DC01            CLIENT01
   Portainer             Active Directory       Domain Joined
    Pi-hole                   DNS               Group Policy
```

---

# Virtual Machines

| Virtual Machine | Operating System | Purpose |
|-----------------|------------------|---------|
| pfSense | pfSense CE | Firewall / Router |
| Ubuntu | Ubuntu Server 24.04 LTS | Docker Host |
| DC01 | Windows Server 2025 | Active Directory Domain Controller |
| CLIENT01 | Windows 11 Pro | Domain Workstation |

---

# Technologies Used

## Virtualization

- Proxmox VE 9.2.3

## Networking

- pfSense
- DNS
- DHCP
- SMB
- TCP/IP

## Windows Infrastructure

- Windows Server 2025
- Active Directory Domain Services
- DNS Server
- Group Policy
- NTFS Permissions
- SMB File Sharing

## Linux

- Ubuntu Server
- Docker
- Docker Compose
- Portainer
- Pi-hole

---

# Completed Projects

## Infrastructure

- [x] Installed Proxmox VE
- [x] Configured virtual networking
- [x] Deployed pfSense Firewall
- [x] Configured LAN/WAN networking
- [x] Installed Ubuntu Server
- [x] Installed Docker
- [x] Installed Portainer
- [x] Installed Pi-hole

---

## Windows Infrastructure

- [x] Deployed Windows Server 2025
- [x] Installed Active Directory Domain Services
- [x] Installed DNS Server
- [x] Created new Active Directory Forest
- [x] Configured DNS
- [x] Created Organizational Units
- [x] Created Security Groups
- [x] Created Domain Users
- [x] Implemented administrative account separation

---

## Windows Client Management

- [x] Installed Windows 11
- [x] Joined workstation to Active Directory
- [x] Verified domain authentication

---

## Group Policy

- [x] Company Wallpaper Deployment
- [x] Drive Mapping
- [x] Password Policies
- [x] Account Lockout Policies
- [x] Software Deployment (7-Zip)

---

## File Services

- [x] Department Shares
- [x] NTFS Permissions
- [x] SMB Shares
- [x] Security Group Access Control

---

# Active Directory Structure

```
newlab.local
│
├── Admin
├── Departments
│   ├── Finance
│   ├── HR
│   ├── IT
│   └── Sales
├── Groups
├── Managed Computers
│   ├── Servers
│   └── Workstations
├── Service Accounts
└── Domain Controllers
```
---

# Group Policy Projects

| Policy | Status |
|---------|--------|
| Company Wallpaper | ✅ |
| Department Drive Mapping | ✅ |
| Password Policy | ✅ |
| Account Lockout Policy | ✅ |
| Software Deployment | ✅ |

---

# Skills Demonstrated

## Windows Server

- Active Directory
- DNS
- Group Policy
- Windows Administration
- Organizational Units
- Security Groups
- Domain Services

## Networking

- DNS
- DHCP
- Firewall Administration
- TCP/IP
- SMB
- Network Troubleshooting

## Security

- Password Policies
- Account Lockout Policies
- Least Privilege Administration
- NTFS Permissions
- Share Permissions

## Virtualization

- Proxmox VE
- Virtual Machine Deployment
- Snapshots
- Virtual Networking

## Linux

- Docker
- Portainer
- Pi-hole
- Ubuntu Server Administration

---

# Troubleshooting Highlights

During this project I resolved numerous enterprise administration issues including:

- Installing VirtIO storage drivers during Windows installation
- Installing VirtIO network drivers
- Resolving APIPA (169.254.x.x) addressing issues
- Configuring Windows Server DNS after Active Directory promotion
- Troubleshooting Windows Update connectivity
- Resolving domain join authentication errors
- Deploying Group Policy successfully
- Configuring SMB shares and NTFS permissions
- Implementing automatic drive mapping
- Deploying software using Group Policy
- Managing Proxmox snapshots

---

# Screenshots

## Infrastructure

- Proxmox Dashboard
- pfSense Dashboard
- Ubuntu Server
- Docker Containers
- Portainer

## Windows Server

- Server Manager
- Active Directory Users and Computers
- DNS Manager
- Group Policy Management

## Active Directory

- Organizational Units
- Users
- Groups
- Workstations OU

## Group Policy

- Company Wallpaper
- Drive Mapping
- Password Policies
- Software Deployment

## Windows Client

- Domain Login
- Wallpaper Applied
- Mapped Network Drives
- Installed Software

---

# Future Projects

- Bulk User Creation with PowerShell
- Active Directory Reporting
- Folder Redirection
- Windows Server Update Services (WSUS)
- Windows Deployment Services (WDS)
- Microsoft Deployment Toolkit (MDT)
- Active Directory Certificate Services (AD CS)
- Network Policy Server (NPS)
- Windows Server Backup
- Wazuh SIEM
- Grafana Monitoring
- Prometheus Monitoring

---

# Lessons Learned

This lab provided hands-on experience deploying and administering enterprise Windows infrastructure from the ground up. Throughout the project I gained practical experience configuring Active Directory, DNS, Group Policy, software deployment, file services, and virtualization while developing troubleshooting skills applicable to real-world IT environments.
