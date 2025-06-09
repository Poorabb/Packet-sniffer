# 🛡️ Network Traffic Analyzer

![Python](https://img.shields.io/badge/Python-3.6%2B-blue.svg)
![Scapy](https://img.shields.io/badge/Scapy-Network%20Sniffer-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A Python tool that captures and analyzes live network traffic to detect potentially **unusual or suspicious network activity** using the [Scapy](https://scapy.net/) library.

---

## 🔍 What Does It Do?

This script:

1. **Captures** live packets from a specified network interface.
2. **Analyzes** the packets to count how many belong to TCP, UDP, ARP, or other protocols.
3. **Detects** IP addresses sending an unusually high number of packets — which may suggest scanning, DDoS, or misconfigured devices.

---

## 💡 Real-World Use Cases

- 🎓 **Learning Networking & Cybersecurity**  
  Understand how network protocols work by observing real traffic.

- 🛡️ **Detect Suspicious Activity**  
  Spot IPs generating too much traffic — a common symptom of scans or attacks.

- 🧪 **Lab Monitoring Tool**  
  Monitor small networks, virtual labs, or Capture The Flag (CTF) environments.

---

## 🧠 How It Works (Internals Explained)

The script is organized into clean functions:

| Function | Purpose |
|---------|---------|
| `capture_packets()` | Uses Scapy to sniff packets from a network interface. |
| `analyze_packets()` | Counts how many packets belong to TCP, UDP, ARP, or other. |
| `detect_unusual_activity()` | Finds IPs sending **100+ packets** during the capture — flagged as unusual. |
| `main()` | Orchestrates the whole process: capture → analyze → detect. |

---

## 📦 Requirements

- Python 3.6+
- Scapy library

### 📥 Installation

```bash
pip install scapy
