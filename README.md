![Banner](screenshots/banner.png)

# 🕷️ NetSpyder – Smart Network Scanner & Analyzer

<p align="center">
  <img src="screenshots/logo.png" width="200">
</p>

---

## 📌 Description
NetSpyder is a powerful and beginner-friendly cybersecurity tool built using Python and Nmap.  
It helps users scan networks, detect connected devices, find open ports, identify operating systems, and generate reports.

---

## ⚙️ Version
**v2.0 ULTIMATE**

---

## 👨‍💻 Author
**Shivansh Kumar**

---

## 🚀 Features
- 🔍 Device Detection  
- 🔓 Full Port Scanning  
- 🖥️ OS Detection  
- 📄 Report Generation  
- 🎨 Stylish Hacker UI  
- ⚡ Fast & Lightweight  

---

## 📸 Screenshots

### 🔹 Main Interface
███╗   ██╗███████╗████████╗███████╗██████╗ ██╗   ██╗██████╗ ███████╗██████╗ 
████╗  ██║██╔════╝╚══██╔══╝██╔════╝██╔══██╗██║   ██║██╔══██╗██╔════╝██╔══██╗
██╔██╗ ██║█████╗     ██║   █████╗  ██████╔╝██║   ██║██████╔╝█████╗  ██████╔╝
██║╚██╗██║██╔══╝     ██║   ██╔══╝  ██╔═══╝ ██║   ██║██╔═══╝ ██╔══╝  ██╔══██╗
██║ ╚████║███████╗   ██║   ███████╗██║     ╚██████╔╝██║     ███████╗██║  ██║
╚═╝  ╚═══╝╚══════╝   ╚═╝   ╚══════╝╚═╝      ╚═════╝ ╚═╝     ╚══════╝╚═╝  ╚═╝

### 🔹 Scanning Output

Enter Target IP (ex: 192.168.1.1/24): 142.250.193.110

Loading Menu...

[1] Device Detection
[2] Port Scan
[3] OS Detection
[4] Full Scan + Report
[5] Tool Info
[6] Exit

Select option: 1

[+] Scanning devices...
100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 100/100 [00:01<00:00, 90.63it/s]
Starting Nmap 7.95 ( https://nmap.org ) at 2026-04-29 06:57 EDT
Nmap scan report for maa05s24-in-f14.1e100.net (142.250.193.110)
Host is up (0.0041s latency).
Nmap done: 1 IP address (1 host up) scanned in 0.10 seconds

---

## 🛠️ Installation (Kali Linux)

```bash
sudo apt update
sudo apt install python3 python3-pip nmap -y
pip install colorama tqdm

