# NETWORK SNIFFER

# 🔐 Network Credential Sniffing

A Python tool to extract plaintext credentials from packet capture (PCAP) files. This project focuses on sniffing credentials for FTP, SMTP, and Telnet protocols using the Scapy library.

> ⚠️ For educational purposes only. Use ethically and responsibly.

## 🛠 Features

- Extracts **FTP** usernames and passwords
- Decodes base64-encoded **SMTP** login data
- Parses **Telnet** login sequences
- Reads from `.pcap` file (e.g., `merged.pcap`)
- Built with [Scapy](https://scapy.readthedocs.io/) for packet analysis

## 🧪 How It Works

1. Load packets from a PCAP file using Scapy.
2. Iterate through TCP packets with payloads.
3. Detect protocol-specific ports:
   - **FTP** (Port 21): `USER`, `PASS`
   - **SMTP** (Port 25): base64-encoded credentials
   - **Telnet** (Port 23): login and password prompts
4. Extract and print detected credentials.

## 🚀 Usage

1. Install required package:

```bash
pip install scapy
