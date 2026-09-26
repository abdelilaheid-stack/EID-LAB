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
- [x] Configure static IP
- [x] Test network connectivity

## 🏢 Phase 2 - Active Directory & DNS

In this phase, EID-DC01 will be configured as a Domain Controller for the EID LAB environment.

### Tasks

- [x] Install Active Directory Domain Services (AD DS)
- [x] Install DNS Server
- [x] Promote EID-DC01 to Domain Controller
- [x] Create a new Active Directory forest
- [x] Configure the domain
- [x] Verify Active Directory and DNS
- [x] Create Organizational Units (OUs)
- [ ] Create users and groups
- [ ] Join Windows 10 client to the domain
- [ ] Test domain authentication

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

### 🌐 Network Connectivity Test

Network connectivity was successfully verified after configuring the static IP address.

Tests performed:

- Ping to default gateway `192.168.196.2` — Successful
- Ping to external IP `8.8.8.8` — Successful
- Packet loss: `0%`

This confirms that EID-DC01 can communicate with both the local network and external networks.

<img width="472" height="546" alt="Screenshot 2026-09-23 230621" src="https://github.com/user-attachments/assets/dd596a37-4180-4531-ad59-22b6fde8b0fd" 

  ## 🏢 Active Directory Domain Services

Installed the **Active Directory Domain Services (AD DS)** role on `EID-DC01`.

This role will allow the server to manage:
- Domain users and computers
- Authentication
- Group Policy
- Centralized network administration

### AD DS Role Installation

<img width="1028" height="772" alt="Screenshot 2026-09-23 232100" src="https://github.com/user-attachments/assets/e2133f57-9505-4183-b558-22ce91fae4d4" 

  
## 🏢 Active Directory Domain Services Deployment

Active Directory Domain Services (AD DS) was installed and the server was promoted to the first Domain Controller in a new forest.

### Configuration

- Server: `EID-DC01`
- Domain: `eid.local`
- NetBIOS name: `EID`
- DNS Server: Enabled
- Global Catalog: Enabled
- Forest Functional Level: Windows Server 2016
- Domain Functional Level: Windows Server 2016

### Deployment Process

1. Installed the **Active Directory Domain Services (AD DS)** role.
2. Selected **Promote this server to a domain controller**.
3. Created a **new forest**.
4. Configured the root domain as `eid.local`.
5. Enabled **DNS Server** and **Global Catalog**.
6. Used `EID` as the NetBIOS domain name.
7. Reviewed the configuration and completed the prerequisite check.
8. Promoted `EID-DC01` to a Domain Controller.
9. Restarted the server and verified the domain configuration.

### Deployment Screenshots

<img width="1625" height="493" alt="Screenshot 2026-09-23 235503" src="https://github.com/user-attachments/assets/e84a82d6-5718-4e2d-82f5-b28583d3d229" />

### ✅ Verification

After the restart, Server Manager confirmed that `EID-DC01` is running as a Domain Controller for the `eid.local` domain.

<img width="1033" height="776" alt="Screenshot 2026-09-23 234419" src="https://github.com/user-attachments/assets/476da847-3a3a-4a0e-b0b4-e85829fd5f53" />

### Active Directory and DNS Verification

Verified that Active Directory and DNS are working correctly.

- Domain: `eid.local`
- Domain Controller: `EID-DC01`
- Active Directory: Operational
- DNS Zones: `eid.local` and `_msdcs.eid.local`
- DNS Server: Local Domain Controller
<img width="1245" height="972" alt="image" src="https://github.com/user-attachments/assets/c96ee679-6aa7-4263-b77d-4f32075600c0" />
<img width="1027" height="773" alt="image" src="https://github.com/user-attachments/assets/b62fbb68-240f-4c25-89bc-e51eb2b0ff91" />
### Organizational Units

Created Organizational Units to organize Active Directory resources:

- `Eid-Users`
- `Eid-Computers`
- `Eid-Groups`
- <img width="1017" height="778" alt="Screenshot 2026-09-26 001938" src="https://github.com/user-attachments/assets/6b2afce4-6f90-44f6-99c9-8ad7ce741f82" />
### Users and Groups

Created Active Directory users and a security group.

- Users: `Ahmad`, `Sara`
- Security Group: `IT-Users`
- Added both users to the `IT-Users` group
<img width="805" height="550" alt="image" src="https://github.com/user-attachments/assets/54c87af8-86ff-4bb9-8226-d33d4058dd8d" />
