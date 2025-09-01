# Multi-Protocol Network Simulation Project  
## 📌 Project Overview
This project demonstrates the **design, simulation, and configuration of a scalable multi-protocol network topology** using **Cisco Packet Tracer**. It integrates **OSPF, EIGRP, RIP**, and also includes **DHCP, NAT, ACLs, Mail Server, and FTP Server configurations**.  

The focus was on:  
- Efficient **subnetting** using **VLSM**.  
- Enabling communication across multiple routing protocols via **route redistribution**.  
- Implementing **NAT** for secure external access.  
- Applying **ACLs** for access restrictions.  
- Configuring **centralized services** such as DHCP, Mail, and FTP servers.  

---

## 🎯 Objectives
1. Simulate a complex network topology using Cisco Packet Tracer.  
2. Apply **VLSM subnetting** to allocate IP addresses efficiently.  
3. Configure and implement routing protocols:  
   - **EIGRP** (Enhanced Interior Gateway Routing Protocol)  
   - **OSPF** (Open Shortest Path First) with **Area 1** and **Area 2**  
   - **RIP** (Routing Information Protocol)  
4. Enable **route redistribution** between protocols.  
5. Configure a **centralized DHCP server** for dynamic IP assignment.  
6. Implement **NAT (Network Address Translation)** for internet access.  
7. Apply **Access Control Lists (ACLs)** for restricted access.  
8. Configure and validate **Mail and FTP servers**.  

---

## 🛠️ Methodology & Implementation Steps
1. **Topology Design**  
   - Replicated logical network layout with routers, switches, servers, and end devices.  
   - Used **color-coded network blocks (A to N)** for organization.  

2. **VLSM Subnetting**  
   - Calculated subnets based on host requirements.  
   - Assigned **/30 subnets** for point-to-point router links to minimize waste.  

3. **Router & Interface Configuration**  
   - Assigned IP addresses to router interfaces.  
   - Configured end devices according to subnet plan.  

4. **Routing Protocols**  
   - **EIGRP**: Configured in **Blocks A & E**.  
   - **OSPF**: Configured in **Blocks B & C**, divided into **Area 1** and **Area 2**.  
   - **RIP**: Configured in **Block G**.  

5. **Route Redistribution**  
   - Implemented between EIGRP–OSPF and OSPF–RIP boundary routers.  

6. **DHCP Configuration**  
   - Centralized DHCP Server in **Block D**.  
   - Assigned IP addresses dynamically to hosts in **Blocks A, B, C, G**.  

7. **NAT Implementation**  
   - Router21 (Network K) and Router10 (Network F) configured for **NAT overload**.  
   - Used public IPs for external access.  

8. **ACL Configuration**  
   - Blocked:  
     - One **PC in Network A** from accessing Web Server.  
     - One **Laptop in Network E**.  
     - One **Smartphone in Network B**.  
     - **All devices in Network D** from Web Server.  

9. **Server Configuration**  
   - **Mail Server (Block D)**:  
     - IP: `192.168.12.10`  
     - Allowed email exchange between **Network H** and **Network I**.  
     - Configured with **SMTP & IMAP**.  
   - **FTP Server (Network G)**:  
     - IP: `192.173.0.4`  
     - Restricted to devices within **Network G** only.  
     - Configured with username/password authentication.  

10. **Testing & Validation**  
    - Verified IP addressing and DHCP lease assignments.  
    - Confirmed routing table correctness and redistribution.  
    - Validated NAT translations with `show ip nat translations`.  
    - Tested ACL restrictions against blocked devices.  
    - Sent/received test emails between Network H & I.  
    - Uploaded files via FTP client from Network G.  

---

## 📡 Network Design & Configuration Details

### 🔹 VLSM Subnetting
- Efficient IP allocation based on host needs.  
- /30 links for router interconnections.  
- Subnets planned to minimize wastage.  

### 🔹 Routing Protocols
- **EIGRP**:  
  - Fast convergence, VLSM support.  
  - Configured with Autonomous System (AS) numbers.  
- **OSPF**:  
  - Hierarchical design with **Area 1 & Area 2**.  
  - Link-state, scalable for large domains.  
- **RIP**:  
  - Distance-vector, simple setup.  
  - Limited to **15 hops**.  

### 🔹 DHCP
- **Central DHCP Server (Block D)** assigns IPs automatically.  
- Simplifies management and reduces configuration errors.  

### 🔹 NAT
- Converts **private IPs → public IPs**.  
- Provides internet access and hides internal addressing.  
- Configured on **Router7 (Network K)** and **Router11 (Network F)**.  

### 🔹 ACLs
- Applied on the router connected to the Web Server.  
- Enforced **granular access restrictions**.  

### 🔹 Servers
- **Mail Server**: Limited to **Network H & I**.  
- **FTP Server**: Limited to **Network G**.  

---

## ✅ Observations & Results
- All **DHCP-configured hosts** received valid IPs.  
- Routing protocols successfully redistributed routes.  
- **NAT translations** verified and functional.  
- ACLs correctly blocked restricted devices/networks.  
- Mail exchange between Network H & I successful.  
- FTP file upload from Network G successful.  

---

## 📸 Screenshots (To Be Added)
- Network topology diagram.  
- Router & switch CLI outputs.  
- DHCP lease allocation.  
- NAT translation verification.  
- ACL hit counters.  
- Mail client test.  
- FTP client test.  

*(Screenshots should be placed in `/screenshots` folder in the repo.)*  

---

## 🔚 Conclusion
This project successfully simulated and validated a **multi-protocol, multi-service network** in Cisco Packet Tracer.  

Key takeaways:  
- **EIGRP, OSPF, and RIP** can coexist with proper **route redistribution**.  
- **NAT** ensures internet connectivity while preserving private addressing.  
- **ACLs** enhance network security by restricting unauthorized access.  
- **Centralized services (DHCP, Mail, FTP)** improve scalability and manageability.  

The final design demonstrates a practical approach to building a **secure, scalable, and well-managed enterprise network**.  

---

## 📂 Repository Structure
