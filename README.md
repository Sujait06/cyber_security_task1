# cyber_security_task1
Task 1: Local Network Port Scanning using nmap

##  Overview
This task is part of the Cyber Security Internship program. The objective is to perform a **TCP SYN scan** on the local network using **Nmap**, identify **open ports and services**, and check for **vulnerabilities** using freely available tools.

---

##  Objective
- Learn basic **network reconnaissance**.
- Discover **open ports** and running **services** on a host within a local subnet.
- Understand the **risks** associated with exposed services.

---

## Tools Used
- ✅ **Nmap** (Port Scanning & Vulnerability Detection)
- ✅ **Wireshark** (for optional packet-level capture)
- ✅ **CMD/Terminal**
- ✅ **GitHub** (for task submission)

---

## 🖧 Network Details
- **Target IP Address:** `192.168.190.93`
- **Scanned Subnet:** `192.168.190.0/24`

---

##  Commands Executed

###  1. TCP SYN Scan (Entire Subnet)
nmap -sS 192.168.190.0/24 -oX scan_result.xml
###  2. Service & Version Detection (Target Host)
nmap -sV 192.168.190.93 -oN service_scan.txt
###  3. Vulnerability Detection (Target Host)
nmap --script vuln 192.168.190.93 -oN vuln_scan.txt
###  4.Optional Wireshark Capture
Interface selected: Wi-Fi
Scan traffic filtered using:
ip.addr == 192.168.190.93 && tcp
Capture saved as: nmap_capture.pcapng
