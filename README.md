# NMAP-Scanning-Project
This project is aimed at identifying devices in a network, uncovering open ports, and checking for vulnerabilities. 

### Step 1 - Identifying Host Ip Address
To scan our device (host) for open ports, we need to identify its IP address.
**Procedure**
* Start NMAP from the CMD terminal.
* Type "ipconfig". This will display all IP addresses; select the interface you are using, in this case, the wireless interface.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5d4cdb38-a0db-457e-af84-7a7482601843" />

### Step 2 - Finding Your Network Range
To find your network range and determine all the IP addresses that are currently connected to the same network(subnet). Type nmap -sn  172.20.10.0/24. Since the host IP is 172.20.10.4, then the network is 172.20.10.0/24
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0648cb4a-2b4c-432b-9ea8-97880bbbf2af" />





