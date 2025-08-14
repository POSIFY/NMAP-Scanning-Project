# NMAP-Scanning-Project
This project is aimed at identifying devices in a network, uncovering open ports, and checking for vulnerabilities. 

### Step 1 - Identifying Host IP Address
To scan our device (host) for open ports, we need to identify its IP address.
**Procedure**
* Start NMAP from the CMD terminal.
* Type "ipconfig". This will display all IP addresses; select the interface you are using, in this case, the wireless interface.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5d4cdb38-a0db-457e-af84-7a7482601843" />

---

### Step 2 - Finding Your Network Range
To find your network range and determine all the IP addresses that are currently connected to the same network(subnet). Type nmap -sn  172.20.10.0/24. Since the host IP is 172.20.10.4, then the network is 172.20.10.0/24

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0648cb4a-2b4c-432b-9ea8-97880bbbf2af" />

---

### Step 3 - Scan for Open Ports
This step involves identifying open ports on the host machine that can lead to an attack or security breach.
**Procedure**
* Select any of the IP addresses in the network.
* Use this nmap command to identify open ports (nmap < HostIPAddress >).

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/84cfd723-ba32-49b9-8f3f-a0655057b141" />

---

### Step 4 - Identify Services
This step involves identifying services on the host machine (target).
To achieve this with nmap, we used the following command: nmap -sV <TargetIPAddress>

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0bd61788-0dbd-45ef-ab2c-59cc6031405b" />

---

### Step 5 - Discovering Service Version Vulnerabilities.
We selected one of the identified services and searched for the version's vulnerabilities: Microsoft Windows RPC.
Below are the results and mitigation recommendations. 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f2c97141-98a9-416d-b7c1-e136a86d71ca" />


**Problem**
Microsoft Windows RPC has a history of severe vulnerabilities, including remote code execution, privilege escalation, and memory corruption flaws. Some are unauthenticated and wormable (e.g., CVE-2022-26809), meaning attackers can compromise systems over the network without user interaction, leading to full control of the target system and possible spread to others.

**Solution**
1. Apply security updates/patches immediately for known RPC vulnerabilities.
2. Restrict RPC access to trusted networks; block unnecessary RPC ports (e.g., TCP 135, 445) at firewalls.
3. Disable unused RPC services and Routing & Remote Access if not needed.
4. Enable network-level authentication and monitor for unusual RPC traffic.






