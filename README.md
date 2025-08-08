# Smart Home IoT Network with RADIUS Authentication (Cisco Packet Tracer)

## 📌 Project Overview
This project is a **Smart Home IoT Network** simulation built using **Cisco Packet Tracer v8.2.0.20400**.  
It demonstrates IoT device management through an **IoT server** and secure authentication using a **RADIUS server**.

The original design used a **Home Gateway** and a **smartphone**.  
In this updated version:
- **Home Gateway** → Removed  
- **IoT Server** → Added  
- **RADIUS Server** → Added  
- **Smartphone** → Replaced with Laptop  
- **Laptop connected to Switch** via Copper Straight Cable  

---

## 🖥️ Network Topology
**Devices Used:**
- 1 x Wireless Router
- 1 x Switch
- 1 x IoT Server
- 1 x RADIUS Server
- 1 x Laptop
- Smart IoT Devices: Smart Light, Smart Fan, Smart Door, Temperature Sensor, Motion Detector

**Connections:**
- Wireless Router connected to Switch (Copper Straight)
- IoT Server connected to Switch (Copper Straight)
- RADIUS Server connected to Switch (Copper Straight)
- Laptop connected to Switch (Copper Straight)
- IoT Devices connected wirelessly via Wireless Router

---

## 🌐 IP Address Plan
| Device           | Interface          | IP Address     | Subnet Mask     | Gateway        |
|------------------|-------------------|----------------|-----------------|---------------|
| Wireless Router  | G0/0              | 192.168.0.1    | 255.255.255.0   | -             |
| Switch           | VLAN 1            | 192.168.0.3    | 255.255.255.0   | 192.168.0.1   |
| IoT Server       | Fa0/0             | 192.168.0.4    | 255.255.255.0   | 192.168.0.1   |
| RADIUS Server    | Fa0/0             | 192.168.0.5    | 255.255.255.0   | 192.168.0.1   |
| Laptop           | Fa0               | DHCP/Static    | 255.255.255.0   | 192.168.0.1   |
| IoT Devices      | Wireless          | DHCP           | 255.255.255.0   | 192.168.0.1   |

---

## ⚙️ Configurations

### 1️⃣ Wireless Router
- Configured DHCP for IoT Devices and Laptop
- Gateway: 192.168.0.1
- Integrated with RADIUS server for authentication

### 2️⃣ IoT Server
- Added all smart devices
- Configured for central IoT management

### 3️⃣ RADIUS Server
- Authentication Protocol: PAP
- Shared Secret: `myradiuskey123`
- User Accounts:
  - **admin1 / adminpass1**
  - **user1 / userpass1**

### 4️⃣ Laptop
- Configured with DHCP (auto IP)
- Verified network and IoT server connectivity

---

## 📂 Project File Structure
