# ICS Security Lab

## Contents
- [Overview](#overview)
- [Architecture](#architecture)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Key Findings](#key-findings)
- [Screenshots](#screenshots)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)

---

## Overview

ICS Security Lab is a simulated Industrial Control System (ICS) cybersecurity environment designed to model real-world Operational Technology (OT) networks using a simplified Purdue Model architecture (Levels 0–3).

The lab demonstrates how industrial environments can be segmented, monitored, and defended against unauthorized access, lateral movement, and insecure protocol activity. Separate zones were created using VLANs and firewall rules to enforce controlled communication paths between operations, SCADA/HMI, and controller networks.

The project also focuses on threat visibility and detection using Wireshark, Zeek, and Suricata while assessing common industrial protocols such as Modbus/TCP and OPC UA.

---

## Architecture

### Purdue Model Zones

- **Level 3:** Operations / Management Workstation  
- **Level 2:** SCADA / HMI Systems  
- **Level 1:** PLC / Controller Simulation  
- **Level 0:** Simulated Sensors / Process Values  
- **Monitoring Zone:** Security Monitoring / IDS Sensors  

### Security Controls

- VLAN-based network segmentation  
- Firewall rules controlling east-west traffic  
- Restricted communication paths between levels  
- IDS monitoring across OT zones  

---

## Features

- Segmented OT zones (Level 0–3)
- Purdue Model network design
- VLAN + firewall isolation
- Modbus/TCP traffic inspection
- OPC UA protocol analysis
- Zeek network telemetry
- Suricata intrusion detection
- Wireshark packet capture and analysis
- Simulated lateral movement testing
- Security hardening recommendations

---

## Tech Stack

- VirtualBox / VMware
- pfSense
- Kali Linux
- Ubuntu Server
- Python
- Wireshark
- Zeek
- Suricata
- Modbus tools
- OPC UA simulation tools

---

## Key Findings

- Plaintext Modbus commands can be observed without encryption
- Flat networks increase risk of lateral movement
- VLAN + firewall segmentation reduces unauthorized access paths
- Suricata successfully detected suspicious scans and probes
- Zeek provided valuable metadata for traffic visibility
- ICS protocols require compensating security controls

---

## Screenshots

_Add screenshots here_

Examples:

- Network topology diagram
- VLAN / firewall rules
- Wireshark Modbus packet capture
- Suricata alerts
- Zeek logs
- SCADA / HMI simulation

---

## How to Run

1. Build virtual machines for each Purdue level
2. Configure VLANs and routing/firewall rules
3. Deploy SCADA / PLC simulation tools
4. Install Zeek and Suricata sensors
5. Generate normal and suspicious traffic
6. Capture and analyze packets with Wireshark
7. Review alerts and document findings

---

## Future Improvements

- Add Splunk or ELK SIEM integration
- Simulate ransomware impact on OT networks
- Implement Zero Trust segmentation
- Add Active Directory environment
- Expand to IEC 62443 mapped controls
- Create attack detection playbooks
- Add cloud-connected industrial asset monitoring

---
```
