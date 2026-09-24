# 🐍 EID LAB

## 🖥️ IT Infrastructure & Cybersecurity Lab

EID LAB is my hands-on IT project for building practical skills in Windows Server, Linux, networking, and cybersecurity.

This repository documents the lab setup, configuration, and troubleshooting.

## 🔧 Lab Environment

- VMware Workstation
- Windows Server 2022
- Windows 10
- Ubuntu Linux
- Kali Linux

## 🎯 Goals

- Build an IT infrastructure from scratch
- Configure Windows Server and Linux systems
- Practice networking and troubleshooting
- Apply security hardening
- Document hands-on work with screenshots

## 🚧 Current Progress

### Phase 1 - Windows Server 2022

- [x] Create Windows Server 2022 VM
- [x] Install Windows Server 2022 with Desktop Experience
- [x] Configure server name
- [ ] Configure static IP
- [ ] Test network connectivity

### 🖥️ VM Hardware Configuration

Configured with:

- 4 GB RAM
- 2 processors
- 60 GB virtual disk
- NAT networking
- Windows Server 2022 installation ISO

<img width="892" height="504" alt="657006925-80e69a01-e8d7-4d75-9b93-6e40859d0024" src="https://github.com/user-attachments/assets/14eeed95-f328-4415-ae3a-8ef966223553" />


### 💿 Windows Server Installation

Windows Server 2022 was successfully installed on VMware Workstation using the Desktop Experience.


<img width="1527" height="741" alt="657351748-92cba34a-2494-41c8-af06-ef46b046b553" src="https://github.com/user-attachments/assets/98dd308f-a150-4a8a-8a83-6f9002cfd417" />

### 🖥️ Server Name Configuration

The Windows Server computer name was successfully changed to **EID-DC01**.

The server is currently configured in the **WORKGROUP** before Active Directory Domain Services deployment.
<img width="1042" height="773" alt="Screenshot 2026-09-23 093221" src="https://github.com/user-attachments/assets/66a625e6-1d07-44d3-833f-3cf2cbbd1ce3" />

### 🌐 Initial Network Configuration

The Windows Server network configuration was verified using `ipconfig /all`.

At this stage, the server was receiving its network configuration automatically from VMware DHCP.

**Current configuration:**

- Hostname: `EID-DC01`
- IPv4 Address: `192.168.196.136`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.196.2`
- DNS Server: `192.168.196.2`
- DHCP: Enabled

The next step is to configure a static IPv4 address for the server before installing and configuring Active Directory Domain Services (AD DS).

<img width="850" height="587" alt="Screenshot 2026-09-23 223830" src="https://github.com/user-attachments/assets/19a35868-6169-47ff-97d3-2ac9ee4ac305" />

### 🌐 Static IP Configuration

A static IPv4 address was configured on the Windows Server to provide a consistent network address for future server roles and services.

- **Server:** EID-DC01
- **IPv4:** 192.168.196.136
- **Subnet Mask:** 255.255.255.0
- **Default Gateway:** 192.168.196.2
- **DNS Server:** 192.168.196.2
- **DHCP:** Disabled

The configuration was verified using:

`ipconfig /all`

<img width="691" height="465" alt="Screenshot 2026-09-23 225649" src="https://github.com/user-attachments/assets/592cb9f7-5061-4100-bbba-e7fd28cca17c" />
