# Cybersecurity Lab Environment Setup — Networkwalks B083C Week 1

## Project Overview

This project documents my Week 1 Cybersecurity Internship task with **Networkwalks**: setting up an isolated virtual cybersecurity lab using **VirtualBox** and **Kali Linux**.

The goal of the lab is to create a controlled environment where cybersecurity concepts and security-testing activities can be practiced without directly affecting a normal host system or external networks.

> **Note:** Configuration values are marked as placeholders where I still need to insert my own verified system and network details. Screenshots will also be added as evidence of my setup.

## Objectives

- Install and configure VirtualBox.
- Set up Kali Linux as a virtual machine.
- Configure the VM's networking.
- Verify communication between the virtual machine and its network gateway.
- Test internet connectivity and DNS resolution.
- Document the setup process and troubleshooting steps.
- Maintain a controlled environment for cybersecurity learning and testing.

## My Lab Environment

| Component | Configuration |
|---|---|
| Host OS | **[Windows version]** |
| CPU | **[Your CPU]** |
| Host RAM | **[Your RAM]** |
| Virtualization Software | VirtualBox **[version]** |
| Guest OS | Kali Linux **[version]** |
| Kali RAM | **[allocated RAM]** |
| Kali CPU | **[allocated CPU cores]** |
| Network Mode | **[NAT / NAT Network]** |
| Network Name | **[network name, if applicable]** |
| Network CIDR | **[your address range]** |
| Kali IP Address | **[your Kali IP]** |
| Default Gateway | **[your gateway]** |
| DNS | **[your DNS]** |

## Lab Architecture

```text
+-----------------------------+
|        Host Computer        |
|        Windows OS           |
|                             |
|        VirtualBox           |
|             |               |
|             v               |
|      +---------------+      |
|      |   Kali Linux  |      |
|      | Virtual Machine|     |
|      +---------------+      |
|             |               |
|        Virtual Network      |
+-----------------------------+
```

The virtual machine provides a separate environment for cybersecurity practice while the host system remains outside the testing activities.

## Lab Setup Procedure

### 1. Prepare the Host System

Before creating the virtual machine, I checked that the system had sufficient resources for running Kali Linux and that hardware virtualization was available.

**Evidence:**

- [ ] Host system information screenshot
- [ ] CPU / RAM screenshot

### 2. Install 7-Zip

7-Zip was used where required to extract compressed files used during the lab setup.

**Evidence:**

- [ ] 7-Zip installation screenshot

### 3. Install VirtualBox

VirtualBox was installed as the virtualization platform used to run Kali Linux.

After installation, I opened VirtualBox and verified that the application could create and manage virtual machines.

**Evidence:**

- [ ] VirtualBox installation screenshot
- [ ] VirtualBox Manager screenshot

### 4. Configure the Virtual Network

The virtual machine was configured with the required networking mode for the lab.

**Network configuration:**

- Network mode: **[your mode]**
- Network name: **[your network name, if applicable]**
- Address range: **[your address range]**

**Evidence:**

- [ ] VirtualBox network configuration screenshot

### 5. Import / Create the Kali Linux VM

Kali Linux was configured as the guest operating system inside VirtualBox.

The VM resources were adjusted according to the available host hardware while leaving enough resources for the Windows host to operate normally.

**VM configuration:**

- RAM: **[your allocated RAM]**
- CPU: **[your allocated CPU cores]**
- Network adapter: **[your adapter configuration]**

**Evidence:**

- [ ] Kali VM settings screenshot
- [ ] Kali Linux desktop screenshot

### 6. Configure and Verify Kali Networking

Inside Kali Linux, I checked the assigned network interface and IP address using:

```bash
ip a
```

I then tested connectivity to the configured gateway:

```bash
ping -c 4 <gateway-ip>
```

Internet connectivity was tested with:

```bash
ping -c 4 8.8.8.8
```

Finally, DNS resolution was checked using:

```bash
nslookup google.com
```

**Evidence:**

- [ ] `ip a` output screenshot
- [ ] Gateway ping screenshot
- [ ] Internet connectivity screenshot
- [ ] DNS test screenshot

## Verification

The following checks were used to confirm that the lab was functioning correctly:

| Test | Expected Result | Status |
|---|---|---|
| Kali receives an IP address | Valid IP assigned | **[Pass/Fail]** |
| Gateway connectivity | Successful ping | **[Pass/Fail]** |
| Internet connectivity | Successful ping to external IP | **[Pass/Fail]** |
| DNS resolution | Domain resolves successfully | **[Pass/Fail]** |
| Nmap available | Nmap version displayed | **[Pass/Fail]** |

To verify Nmap:

```bash
nmap --version
```

## Problems Encountered & Troubleshooting

### 1. Network Option Missing in VirtualBox

One of the issues I encountered during the setup was that the **Network** option shown in the tutorial was not appearing in my VirtualBox Manager.

This meant I could not immediately follow the same network configuration steps shown in the guide.

I investigated the VirtualBox installation and configuration rather than assuming that the tutorial interface would be identical to my installation.

**What I learned:**

VirtualBox features and management options can depend on the installed version, installation state, and enabled components. When following a tutorial, the interface may not always match exactly, so checking the actual installation and configuration is important.

**Evidence:**

- [ ] Screenshot showing the missing Network option
- [ ] Screenshot of the troubleshooting / installation state
- [ ] Screenshot showing the final working configuration

### 2. VirtualBox Installer Issue

While trying to resolve the missing networking option, I modified the VirtualBox installation and encountered an installer screen offering **Repair** or **Remove**. I also received an error stating that the installer had **ended prematurely**.

This became an additional troubleshooting step during the lab setup.

**Resolution:**

**[Insert the exact steps that finally fixed the issue here.]**

**Evidence:**

- [ ] Installer Repair/Remove screenshot
- [ ] Installer error screenshot
- [ ] Final successful installation screenshot

## Screenshots / Evidence

The following evidence will be added to this repository:

```text
screenshots/
├── host-system.png
├── virtualbox-manager.png
├── virtualbox-network.png
├── kali-settings.png
├── kali-desktop.png
├── kali-ip-address.png
├── gateway-ping.png
├── internet-connectivity.png
├── dns-test.png
└── troubleshooting/
    ├── network-option-missing.png
    └── installer-error.png
```

Screenshots should show the actual configuration used for this project rather than example values from other lab repositories.

## What I Learned

Through this setup, I gained practical experience with:

- Virtual machine deployment using VirtualBox.
- Kali Linux as a cybersecurity-focused operating system.
- Basic Linux networking commands.
- IP addressing and default gateways.
- DNS resolution testing.
- Virtual networking concepts.
- Troubleshooting virtualization software.
- The importance of documenting technical issues and their solutions.

The troubleshooting process was particularly useful because it showed that real-world setup does not always match a tutorial step-for-step.

## Security & Ethical Use

This lab is intended strictly for **authorized cybersecurity learning and testing**.

Any penetration testing, scanning, exploitation, or other security activity performed using this environment should only target systems for which I have explicit permission.

The purpose of the isolated lab is to provide a controlled environment for learning without intentionally affecting systems or networks that I do not own or have authorization to test.

## Tools & Technologies

- Windows
- VirtualBox
- Kali Linux
- 7-Zip
- Nmap
- Linux networking utilities

## Project Information

**Program:** Cybersecurity Internship — Networkwalks  
**Batch:** B083C  
**Week:** 1  
**Project:** Cybersecurity Lab Environment Setup

**Author:** bor-ee-d

## Disclaimer

This repository documents a personal cybersecurity learning environment created for educational and authorized testing purposes. No unauthorized systems should be targeted using the techniques or tools discussed in this project.
