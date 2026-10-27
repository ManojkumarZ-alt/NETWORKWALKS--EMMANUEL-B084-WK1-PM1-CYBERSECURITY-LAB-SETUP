# NETWORKWALKS--EMMANUEL-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP
Cybersecurity Lab Environment Setup using Windows, VirtualBox, and Kali Linux | NetworkWalks Internship
## Week 1 – PM1: Cybersecurity Lab Setup

### 1. Project Overview

This repository documents my cybersecurity lab environment setup as part of my internship at NetworkWalks. The lab uses Kali Linux running in Oracle VirtualBox on a Windows host system.

The purpose of this task is to document the lab configuration, understand basic Linux system information, inspect network settings, and verify the environment before performing further cybersecurity exercises.

### 2. Objectives

- Set up and document a Kali Linux lab environment.
- Identify the operating system and available system resources.
- Understand network interfaces, IP addressing, and routing.
- Check available memory and disk space.
- Maintain a record of commands and verification results.

### 3. Lab Environment

| Component | Verified details |
|---|---|
| Host operating system | Windows 10/11 (exact version not yet recorded) |
| Virtualization software | Oracle VirtualBox |
| Guest operating system | Kali GNU/Linux Rolling |
| Kali version | 2026.3 |
| Network interface | eth0 |
| IPv4 address | 10.0.2.15/24 |
| Default gateway | 10.0.2.2 |
| Reported memory | 4.4 GiB |
| Root filesystem size | 42 GB |
| Root filesystem usage | 16 GB used, 25 GB available |

### 4. System Information and Verification

#### 4.1 Operating System

Command:

```bash
cat /etc/os-release
```

Result: The command identified the guest operating system as Kali GNU/Linux Rolling, version 2026.3.

#### 4.2 Network Interface Configuration

Command:

```bash
ip addr
```

Result: The `eth0` interface was active and had the IPv4 address `10.0.2.15/24`. The loopback interface was also present.

#### 4.3 Routing Configuration

Command:

```bash
ip route
```

Result: The routing table showed a default route through `10.0.2.2` using `eth0`, along with the directly connected network `10.0.2.0/24`.

#### 4.4 Memory Usage

Command:

```bash
free -h
```

Result: The system reported 4.4 GiB of total memory and approximately 3.5 GiB available at the time of checking.

#### 4.5 Disk Space

Command:

```bash
df -h
```

Result: The root filesystem `/dev/sda1` had a reported size of 42 GB, with approximately 16 GB used and 25 GB available.

### 5. Initial Findings

The initial checks confirmed that Kali Linux was running and that its network interface had an IPv4 address and a configured default route. System memory and filesystem information were also collected successfully.

The IP address and gateway are consistent with the default VirtualBox NAT address range. The VirtualBox adapter mode and external network connectivity will be verified separately.

### 6. Challenges and Solutions

The initial challenge was clipboard sharing between Windows and Kali Linux in VirtualBox. Troubleshooting the shared clipboard and guest integration will be documented after the issue is resolved.

### 7. Learning Outcomes

- Learned how to identify Linux operating system details.
- Practiced inspecting network interfaces using `ip addr`.
- Understood the purpose of the default route using `ip route`.
- Learned to check memory and disk usage using `free -h` and `df -h`.
- Gained experience documenting system configuration for a cybersecurity lab.

### 8. Next Steps

- Verify VirtualBox network adapter settings.
- Test network connectivity.
- Capture screenshots of the system configuration and verification commands.
- Document the remaining lab setup and future authorized cybersecurity exercises.

### 9. Ethical Use

This lab is intended for cybersecurity education and authorized testing only. Any future scanning or security testing will be restricted to systems for which permission has been obtained.

### 10. Author

Prepared as part of the NetworkWalks Cybersecurity Internship.

**Status:** Initial system and network information collected.
