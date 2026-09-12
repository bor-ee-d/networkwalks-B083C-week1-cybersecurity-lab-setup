# Cybersecurity Lab Environment Setup — Networkwalks B083C Week 1

## Project Overview

This project documents my Week 1 Cybersecurity Internship task with **Networkwalks**: setting up a cybersecurity lab using **VirtualBox** and **Kali Linux**.

The goal of the lab is to create a controlled environment where cybersecurity concepts and security-testing activities can be practiced safely.

## Objectives

- Install and configure VirtualBox.
- Set up Kali Linux as a virtual machine.
- Configure the Kali VM resources.
- Document the setup process and troubleshooting steps.
- Maintain a controlled environment for cybersecurity learning and testing.

## My Lab Environment

| Component | Configuration |
|---|---|
| Host OS | **10.0.26200 Build 26200** |
| CPU | **CPU Intel(R) Core(TM) Ultra 7 155H** |
| Host RAM | **16.0 GB** |
| Virtualization Software | VirtualBox **Version 7.2.16 r174877 (Qt6.8.0 on windows)**|
| Guest OS | Kali Linux **Debian (64-bit)** |
| Kali RAM | **4 MB ---> 16364 MB** |
| Kali CPU | **1 CPU ---> 32 CPUs** |
| Network Adapter | **NAT Network** |

The virtual machine provides a separate environment for cybersecurity practice while the host system remains outside the testing activities.

### 1. Lab Setup Procedure

### 1. Prepare the Host System

Before creating the virtual machine, I checked that the system had sufficient resources for running Kali Linux and that hardware virtualization was available.

**Evidence:**

- <img width="1480" height="1418" alt="image" src="https://github.com/user-attachments/assets/15b9cd88-1e2d-4056-b4ef-56c9f1559a7f" />

- <img width="2156" height="1160" alt="image" src="https://github.com/user-attachments/assets/95f60962-3781-4e01-849f-10df98ce0a05" />

### 2. Install 7-Zip

7-Zip was used where required to extract compressed files used during the lab setup.

**Evidence:**

- <img width="1462" height="872" alt="image" src="https://github.com/user-attachments/assets/13b564ae-7fcb-4087-97bc-5fb63bb3c9b8" />

### 3. Install VirtualBox

VirtualBox was installed as the virtualization platform used to run Kali Linux.

After installation, I opened VirtualBox and verified that the application could create and manage virtual machines.

**Evidence:**

- <img width="1972" height="1242" alt="image" src="https://github.com/user-attachments/assets/a0487bba-9842-4ce4-83a0-dbff26a43c5a" />

- <img width="1826" height="1170" alt="image" src="https://github.com/user-attachments/assets/e24ebc46-5b49-4ebe-aff4-aa7ca1174eb8" />

### 4. Import / Create the Kali Linux VM

Kali Linux was configured as the guest operating system inside VirtualBox.

The VM resources were adjusted according to the available host hardware while leaving enough resources for the Windows host to operate normally.

**VM configuration:**

- RAM: **[your allocated RAM]**
- CPU: **[your allocated CPU cores]**
- Network adapter: **[your adapter configuration]**

**Evidence:**

- [ ] Kali VM settings screenshot
- [ ] Kali Linux desktop screenshot

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
├── kali-settings.png
├── kali-desktop.png
└── troubleshooting/
    ├── network-option-missing.png
    └── installer-error.png
```

Screenshots should show the actual configuration used for this project rather than example values from other lab repositories.

## What I Learned

Through this setup, I gained practical experience with:

- Virtual machine deployment using VirtualBox.
- Kali Linux as a cybersecurity-focused operating system.
- Allocating VM resources appropriately.
- Troubleshooting virtualization software.
- The importance of documenting technical issues and their solutions.

The troubleshooting process was particularly useful because it showed that real-world setup does not always match a tutorial step-for-step.

## Security & Ethical Use

This lab is intended strictly for **authorized cybersecurity learning and testing**.

Any penetration testing, scanning, exploitation, or other security activity performed using this environment should only target systems for which I have explicit permission.

The purpose of the lab is to provide a controlled environment for learning without intentionally affecting systems or networks that I do not own or have authorization to test.

## Tools & Technologies

- Windows
- VirtualBox
- Kali Linux
- 7-Zip

## Project Information

**Program:** Cybersecurity Internship — Networkwalks  
**Batch:** B083C  
**Week:** 1  
**Project:** Cybersecurity Lab Environment Setup

**Author:** bor-ee-d

## Disclaimer

This repository documents a personal cybersecurity learning environment created for educational and authorized testing purposes. No unauthorized systems should be targeted using the techniques or tools discussed in this project.
