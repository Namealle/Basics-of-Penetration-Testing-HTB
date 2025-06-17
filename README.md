# 🔐 Hack The Box - FTP Anonymous Access Writeup

> **Difficulty:** 🟢 Beginner  
> **Platform:** Hack The Box  
> **Type:** Walkthrough  
> **Author:** Namealle  
> **Date:** 2025-06-16

---

## 🎯 Target Info

- **Target IP:** `129.10.55.123`
- **Service in focus:** FTP (Port 21)
- **Goal:** Gain access via anonymous FTP and retrieve the flag

---

## 🧪 Step-by-Step Walkthrough

### 1. ✅ Check if the machine is alive

Use `ping` to test connectivity.

---
ping 129.10.55.123
### 2. 🔍 Scan for open ports
Run a basic and version detection scan with nmap:

---
sudo nmap 129.10.55.123
sudo nmap -sV 129.10.55.123
✅ Port 21 (FTP) was found open and supports anonymous login.

###3. 📥 Install FTP Client (if needed)
If FTP client is not installed, run:

---
sudo apt install ftp -y
###4. 🔑 Connect to FTP
Connect to the FTP server:

---
ftp 129.10.55.123
Login credentials:

Username: anonymous

Password: anon123 or leave it blank

###5. 🧭 Use FTP Commands
Helpful FTP commands:

---
help            # List available commands
ls              # View files
cd <folder>     # Navigate to a directory (if needed)
get flag.txt    # Download the flag file
bye             # Exit the FTP session
###6. 🏁 Capture the Flag
After downloading the flag, display its contents:

---
cat flag.txt
🎉 Flag: 035db21c881520061c53e0536e44f815

📚 Lessons Learned
Anonymous FTP access is a serious misconfiguration.

Simple tools like nmap and ftp can uncover sensitive data.

Always check for default or anonymous logins on open services.

📦 Tools Used
nmap

ftp

Kali Linux
