# 📡 Project 1: Design and Implementation of a Small Office Home Office Network (SOHO)

## 📝 Case Study and Requirements

XYZ Company is a fast-growing enterprise based in Eastern Australia, serving over 2 million customers globally. The company specializes in buying and selling food products, with operations centralized at its headquarters.

To expand operations, XYZ Company plans to open a branch near the local village of **Bonalbo**. This branch will operate **independently** from the headquarters' network. As a result, the company has assigned the task of designing the network to a young IT graduate.

### 📋 Requirements:

- One router and one switch to be used (All **CISCO** devices)
- Three departments:
  - **Admin/IT**
  - **Finance/HR**
  - **Customer Service/Reception**
- Each department must be assigned a **different VLAN**
- Each department should have its own **wireless network**
- All host devices must receive **IPv4 addresses automatically** (via DHCP)
- All devices across departments should be able to **communicate**
- The base network assigned by the ISP: `192.168.1.0/24`

---

## 🎯 Objective

To design and implement a secure, efficient, and scalable SOHO network infrastructure for the new branch of XYZ Company, using Cisco devices, while meeting all given technical and business requirements.

---

## 🔧 Technologies & Configurations Implemented

- ✅ Created a basic network using a **Cisco Router** and **Access Layer Switch**
- ✅ Connected networking devices using appropriate **cabling**
- ✅ Configured **VLANs** and assigned VLAN IDs to switch ports
- ✅ Performed **Subnetting and IP addressing** for efficient allocation
- ✅ Configured **Inter-VLAN Routing** using **Router-on-a-Stick**
- ✅ Set up the **DHCP Server** on the router to assign IPs dynamically
- ✅ Configured **Wireless Access Points** for departmental Wi-Fi
- ✅ Applied **Host Device Configurations** for all end devices
- ✅ **Tested and Verified** network connectivity across VLANs

---
# 📡 Detailed Network Implementation - XYZ Company (SOHO Design)

This document outlines the network implementation plan for XYZ Company's branch office. The design follows a **SOHO (Small Office/Home Office)** model using structured segmentation with VLANs, Inter-VLAN Routing, DHCP, and wireless setup.

---

## 🔸 Network Design Summary

- **Router:** Cisco 2911  
- **Switch:** Cisco 2960-24TT  
- **Departments and VLANs:**
  - **Admin/IT** → VLAN 10 → `192.168.1.0/26`
  - **HR/Finance** → VLAN 20 → `192.168.1.64/26`
  - **Customer Service/Reception** → VLAN 30 → `192.168.1.128/26`

---

## 📐 Subnetting Plan (Based on `192.168.1.0/24`)

| VLAN | Department             | Subnet            | Range Start - End         | Broadcast       |
|------|------------------------|-------------------|---------------------------|-----------------|
| 10   | Admin / IT             | 192.168.1.0/26    | 192.168.1.1 - 192.168.1.62| 192.168.1.63    |
| 20   | HR / Finance           | 192.168.1.64/26   | 192.168.1.65 - 192.168.1.126| 192.168.1.127 |
| 30   | CS / Reception         | 192.168.1.128/26  | 192.168.1.129 - 192.168.1.190| 192.168.1.191 |

---

## 🛠️ Devices Configured Per VLAN

### 🔹 VLAN 10 – Admin/IT
- 1 PC (`PC0`)
- 1 Laptop (`Laptop0`)
- 1 Access Point (`Access Point1`) – Wireless for `Smartphone0`
- 1 Printer (`Printer0`)
- **Subnet:** `192.168.1.0/26`

---

### 🔹 VLAN 20 – Finance/HR
- 1 PC (`PC1`)
- 1 Laptop (`Laptop1`)
- 1 Access Point (`Access Point0`) – Wireless for `Smartphone3`
- 1 Printer (`Printer1`)
- **Subnet:** `192.168.1.64/26`

---

### 🔹 VLAN 30 – Customer Service/Reception
- 1 PC (`PC2`)
- 1 Access Point (`Access Point2`) – Wireless for `Smartphone2` and `TabletPC0`
- 1 Printer (`Printer2`)
- **Subnet:** `192.168.1.128/26`


## 📌 Outcome

This project reinforced practical knowledge in:

- Enterprise-level **LAN design**
- **VLAN segmentation** and logical separation
- **Dynamic IP address allocation**
- Real-world application of **Cisco routing and switching concepts**
- End-to-end **network connectivity validation**

---

## 🧠 Tools Used

- Cisco Packet Tracer
- Cisco Router & Switch CLI
- Subnetting Calculator (manual)



