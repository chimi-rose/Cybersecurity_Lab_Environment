# Hello, I'm Chimé (Chimi) Lhamo 
### Aspiring Cybersecurity Analyst

I am a security-focused CIS major college graduate currently building a hands-on research laboratory to simulate real-world attack and defense scenarios.

## Connect with me:
www.linkedin.com/in/chimi-rlhamo

---

## My Lab Environment
My primary research is conducted in a virtualized, segregated environment:
* **Hypervisor:** VirtualBox
* **Attacker:** Kali Linux
* **Network:** Isolated NAT Network 'SecurityLab' (10.0.2.0/24). This segmentation ensures that the host router is protected from any malicious script that escapes from the VM environment.
* **Attacker IP (Kali):** 10.0.2.15
* **Goal:** Documentation of vulnerability research and network auditing.

---

## Phase 1: Network Discovery (Nmap)
**Target:** `scanme.nmap.org`  
**Command:** `nmap -F scanme.nmap.org`, 'nmap -sV -T4 -p 22,80 scanme.nmap.org -oN nmap_scan_results.txt'

### Key Findings:
* **SSH (Port 22):** Open. Identified as a potential remote access point. Identifying the specific OS running on this port (Ubuntu 2, Ubuntu 2.13) by running the -sV command allows for ruther investigation into potential vulnerabilities known to these versions.
* **HTTP (Port 80):** Open. Confirmed a web server is running. 
* **Filtered Ports:** 98 ports returned as `filtered`, indicating an active firewall or packet filter is protecting the host.
