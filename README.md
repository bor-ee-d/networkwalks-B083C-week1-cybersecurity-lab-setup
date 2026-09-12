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

- <img width="1920" height="1504" alt="image" src="https://github.com/user-attachments/assets/16f8524b-7f34-4c0e-9b36-f8e38d9b5638" />

### 4. Import / Create the Kali Linux VM

Kali Linux was configured as the guest operating system inside VirtualBox.

The VM resources were adjusted according to the available host hardware while leaving enough resources for the Windows host to operate normally.

**VM configuration:**

- RAM: **4 MB ---> 16364 MB**
- CPU: **1 CPU ---> 32 CPUs**
- Network adapter: **Nat Network**

**Evidence:**

- <img width="2880" height="1796" alt="image" src="https://github.com/user-attachments/assets/b1b5d019-d058-4c04-a8f3-a30dee339bc0" />

- <img width="1826" height="1170" alt="image" src="https://github.com/user-attachments/assets/c71e6da9-d17d-4821-aa2d-4985388e731a" />

## 5. Configuring the Virtual Network

I configured the virtual networking required for the cybersecurity lab.

The network was configured as:

Network Type: NAT Network
Network Name: Natnetwork
IPv4 Network: Manual
DHCP: Enabled

This network configuration provides a controlled environment for the virtual machines used in the lab.

- <img width="1832" height="1168" alt="Screenshot 2026-09-11 180609" src="https://github.com/user-attachments/assets/feb82417-fa8d-49e1-b5b4-9a756a03b277" />

## Problems Encountered & Troubleshooting

### 1. Network Option Missing in VirtualBox

One of the issues I encountered during the setup was that the **Network** option shown in the tutorial was not appearing in my VirtualBox Manager.

This meant I could not immediately follow the same network configuration steps shown in the guide.

I investigated the VirtualBox installation and configuration rather than assuming that the tutorial interface would be identical to my installation.

**What I learned:**

VirtualBox features and management options can depend on the installed version, installation state, and enabled components. When following a tutorial, the interface may not always match exactly, so checking the actual installation and configuration is important.

**Evidence:**

- <img width="1936" height="1511" alt="image" src="https://github.com/user-attachments/assets/a64ee9e6-7f5e-46b0-9991-5be9d89aedc7" />

- <img width="980" height="762" alt="image" src="https://github.com/user-attachments/assets/56f430ad-1e3b-46d9-a73c-93ea53b4a39e" />

Before configuration and repair

- <img width="1928" height="1480" alt="image" src="https://github.com/user-attachments/assets/67fb379f-0a45-479c-8b53-e9195f7ca284" />

After configuration and repair

- <img width="1920" height="1482" alt="image" src="https://github.com/user-attachments/assets/0e31af4c-fc57-4112-87d7-cf0dfe34d97d" />

### 2. VirtualBox Installer Issue

While trying to resolve the missing networking option, I modified the VirtualBox installation and encountered an installer screen offering **Repair** or **Remove**. I also received an error stating that the installer had **ended prematurely**.

This became an additional troubleshooting step during the lab setup.

**Resolution:**

The resolution was rather complicated as I tried **multiple strategies** to get the network option to show when I got to **File --> Tools --> (supposed to find network but not available but every other option is shown)**. For resolving this issue I **uninstalled the VM** and then **restarted my pc** and then **reinstalled it** but that still didn't fix the issue thats when I **opened the installer** and **opted for repair** and then again **restarted my pc** and checked and that too didn't fix the issue then I thought it would probably appear on its own after a while and **went forward with the next steps and after adding the new Kali Linux VM the network option appeared on its own probably because it took time to show up in the options**.

**Evidence:**

- <img width="982" height="774" alt="image" src="https://github.com/user-attachments/assets/9000ae7a-0de0-4c1a-9a51-3f9da85cbede" />

- <img width="980" height="762" alt="image" src="https://github.com/user-attachments/assets/940f24bd-c08a-4d57-95b6-31ab96a6780e" />

- <img width="1024" height="813" alt="image" src="https://github.com/user-attachments/assets/a44f8a61-a511-4222-8674-6980a96cdbc2" />

## Screenshots / Evidence

The following evidence will were added to this repository:

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

Screenshots show the actual configuration used for this project rather than example values from other lab repositories.

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
