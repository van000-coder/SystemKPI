# SystemKPI
Hi This is a system file similar to DPI (created for testing your bypass services)
#SystemKPI

A powerful experimental network system tool written in Go.  
Designed for testing firewall behavior, analyzing traffic patterns, and simulating unstable or restricted network environments.

---

## Features

### Firewall Control
- nftables-based firewall management
- Default **DROP policy**
- Whitelist (trusted IPs/domains)
- Blocks UDP traffic
- Allows only HTTP/HTTPS (80/443)
- Custom rule injection



### Traffic Analysis
- Real-time packet capture using gopacket
- Tracks:
  - Top IP addresses
  - Top ports
- Lightweight network monitoring



### Live Dashboard
- Built-in Web UI (`localhost:8080`)
- Real-time traffic graph (Chart.js)
- Live statistics updates
- No external frontend dependencies



### Smart Monitoring
- Tracks connection behavior
- Visualizes traffic spikes
- Useful for:
  - Network experiments
  - Firewall testing
  - Traffic observation


## Demo Interface

- Web-based control panel
- Add trusted IPs/domains
- Enable/disable firewall
- View live traffic stats

---

## Requirements

- Linux (recommended)
- Go 1.20+
- libpcap
- nftables
- root privileges

---
## ⚠️Disclaimer⚠️ 

This tool is intended for:

educational purposes
network experimentation
local testing environments
Do NOT use it on networks or systems without proper authorization.

⚠️THE AUTHOR IS NOT RESPONSIBLE FOR ITS USE⚠️
⚠️THE AUTHOR IS NOT RESPONSIBLE FOR ITS USE⚠️
⚠️THE AUTHOR IS NOT RESPONSIBLE FOR ITS USE⚠️
## Installation

```bash
sudo apt update
sudo apt install golang libpcap-dev nftables

go mod init network-lab
go get github.com/google/gopacket
sudo go run network_lab_ultra.go

Open in browser:

http://localhost:8080

Build Binary
go build -o network-lab
sudo ./network-lab
