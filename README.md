from colorama import Fore, Style, init
from tqdm import tqdm
import time
import os
import datetime

init()

TOOL_NAME = "NetSpyder"
VERSION = "2.0 ULTIMATE"
AUTHOR = "Shivansh Kumar"

# 🔥 Loading Animation
def loading(text):
    print(Fore.YELLOW + f"\n{text}" + Style.RESET_ALL)
    for _ in tqdm(range(100)):
        time.sleep(0.01)

# 🕷️ Banner
def banner():
    os.system("clear")
    print(Fore.GREEN + """
███╗   ██╗███████╗████████╗███████╗██████╗ ██╗   ██╗██████╗ ███████╗██████╗ 
████╗  ██║██╔════╝╚══██╔══╝██╔════╝██╔══██╗██║   ██║██╔══██╗██╔════╝██╔══██╗
██╔██╗ ██║█████╗     ██║   █████╗  ██████╔╝██║   ██║██████╔╝█████╗  ██████╔╝
██║╚██╗██║██╔══╝     ██║   ██╔══╝  ██╔═══╝ ██║   ██║██╔═══╝ ██╔══╝  ██╔══██╗
██║ ╚████║███████╗   ██║   ███████╗██║     ╚██████╔╝██║     ███████╗██║  ██║
╚═╝  ╚═══╝╚══════╝   ╚═╝   ╚══════╝╚═╝      ╚═════╝ ╚═╝     ╚══════╝╚═╝  ╚═╝
""" + Style.RESET_ALL)

    print(Fore.CYAN + f"""
        🕷️ {TOOL_NAME}
        Version: {VERSION}
        Author: {AUTHOR}
""" + Style.RESET_ALL)

# 🎯 Functions
def scan_devices(target):
    loading("[+] Scanning devices...")
    os.system(f"nmap -sn {target}")

def port_scan(target):
    loading("[+] Scanning all ports...")
    os.system(f"nmap -p- {target}")

def os_detection(target):
    loading("[+] Detecting OS...")
    os.system(f"nmap -O {target}")

def full_scan(target):
    loading("[+] Running advanced scan...")
    filename = f"report_{datetime.datetime.now().strftime('%Y%m%d_%H%M%S')}.txt"
    os.system(f"nmap -A {target} -oN {filename}")
    print(Fore.GREEN + f"\n[+] Report saved as {filename}" + Style.RESET_ALL)

# 🎮 Menu Animation
def show_menu():
    menu = [
        "[1] Device Detection",
        "[2] Port Scan",
        "[3] OS Detection",
        "[4] Full Scan + Report",
        "[5] Tool Info",
        "[6] Exit"
    ]

    print(Fore.MAGENTA + "\nLoading Menu...\n" + Style.RESET_ALL)
    for item in menu:
        print(Fore.YELLOW + item + Style.RESET_ALL)
        time.sleep(0.2)

# 📌 Tool Info
def tool_info():
    print(Fore.CYAN + f"""
Tool Name : {TOOL_NAME}
Version   : {VERSION}
Author    : {AUTHOR}
Purpose   : Network Scanning & Analysis
""" + Style.RESET_ALL)

# 🚀 Main Program
def main():
    banner()
    target = input(Fore.GREEN + "\nEnter Target IP (ex: 192.168.1.1/24): " + Style.RESET_ALL)

    while True:
        show_menu()
        choice = input(Fore.GREEN + "\nSelect option: " + Style.RESET_ALL)

        if choice == "1":
            scan_devices(target)
        elif choice == "2":
            port_scan(target)
        elif choice == "3":
            os_detection(target)
        elif choice == "4":
            full_scan(target)
        elif choice == "5":
            tool_info()
        elif choice == "6":
            print(Fore.RED + "Exiting NetSpyder..." + Style.RESET_ALL)
            break
        else:
            print(Fore.RED + "Invalid choice!" + Style.RESET_ALL)

if __name__ == "__main__":
    main()
