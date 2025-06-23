# Task 1: Scan Your Local Network for Open Ports

##  Steps Performed

1. **Determine Your Local IP Range**
   
   ip a
   
   (Identify the subnet, e.g., `192.168.1.0/24`.)

2. **Perform a TCP SYN Scan**
   
   sudo nmap -sS 192.168.1.0/24
   
   (This identifies active hosts and open TCP ports stealthily).

3. **Save Scan Results**
   
   nmap -sS 192.168.1.0/24 -oN scan_results.txt
   

4. **(Optional) Capture Network Traffic with Wireshark**
   - Open Wireshark.
   - Select your network interface.
   - Apply a display filter like: `tcp.port == 80`.
   - Run your Nmap scan concurrently to observe packets.

5. **Research Common Services**
   Review open ports and their associated services. Use:
   
   nmap -sV <target-ip>
   

6. **Analyze and Identify Potential Risks**
   - Determine if unnecessary ports/services are open.
   - Note outdated or vulnerable services.
