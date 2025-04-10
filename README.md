# 🔒 Securing the Router for Administrative Access

This project simulates a secure network environment using **Cisco Packet Tracer**. The focus is on configuring administrative access to routers with strong security practices, such as SSH, encrypted passwords, and user authentication policies.

## 🖥️ Topology Overview

The network includes:
- **3 Routers** (R1, R2, R3)
- **2 PCs** (PC-A, PC-C)
- **3 Switches** (S1, S2, S3)

Each device is connected and addressed according to the following IP addressing scheme:

| Device | Interface | IP Address | Subnet Mask | Connected Port |
|--------|-----------|------------|-------------|----------------|
| R1     | G0/1      | 172.16.1.1 | 255.255.255.0 | S1 F0/5 |
| R1     | S0/0/0    | 10.1.1.1   | 255.255.255.252 | N/A |
| R2     | S0/0/0    | 10.1.1.2   | 255.255.255.252 | N/A |
| R2     | S0/0/1    | 10.2.2.2   | 255.255.255.252 | N/A |
| R3     | S0/0/1    | 10.2.2.1   | 255.255.255.252 | N/A |
| R3     | G0/1      | 172.16.3.1 | 255.255.255.0 | S3 F0/5 |
| PC-A   | NIC       | 172.16.1.3 | 255.255.255.0 | Gateway: 172.16.1.1 |
| PC-C   | NIC       | 172.16.3.3 | 255.255.255.0 | Gateway: 172.16.3.1 |

## 🔧 Configuration Highlights

The routers are secured with the following administrative settings:

- **Console Password**: `ciscovistula55`
- **VTY Line Password**: `ciscovtypa123`
- **Enable Password**: `cisco12345`
- **Local User**: `Admin007`  
  **Secret Password**: `Admin007pass`

### ✅ Security Features Implemented

- All passwords are encrypted using `service password-encryption`.
- SSH access configured (Version 2) with:
  - Timeout: **90 seconds**
  - Authentication retries: **2**
- Exec-timeout set to **4 minutes** (auto-logout).
- Password minimum length set to **10 characters**.
- **MOTD Banner**:
  ```
  No Unauthorized Access!
  ```
- Syslog server configured for logging.

## 📁 Files Included

- `Securing_Router.pkt` — Complete Packet Tracer project.
- `README.md` — This file with setup and documentation.

## 🚀 Getting Started

To open and run this project:

1. Download and install **Cisco Packet Tracer**.
2. Clone this repo or download the ZIP.
3. Open `Securing_Router.pkt` in Packet Tracer.
4. Explore device configurations and test connectivity and SSH access between hosts.
