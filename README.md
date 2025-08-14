# Capture-and-Analyze-Network-Traffic-Using-Wireshark

## Objective
Capture live network packets and identify basic protocols and traffic types.

## Tools Used
- Wireshark 

## Steps Performed
1. Opened Wireshark and selected the active network interface.
2. Started live packet capture.
3. Generated network activity:
   - Browsed websites (HTTP)
     google.com
   - Used ping to create ICMP traffic
     ```
     ping youtube.com
     ping google.com
     ping bing.com
     ```
4. Stopped the capture after generating enough traffic.
5. Applied protocol filters to identify specific types of traffic:
   - `http` → Web browsing traffic
   - `dns` → Domain name lookups
   - `tcp` → Transport layer protocol for HTTP and others
   - `arp` → Address resolution protocol for mapping IP to MAC addresses
   - `icmp` → Ping requests and replies
6. Saved the capture as `capture.pcapng`.

## Protocols Identified
1. **HTTP** — Unencrypted web browsing traffic, showing GET requests and responses.
2. **DNS** — Domain resolution queries.
3. **TCP** — Transport protocol ensuring reliable delivery of packets.
4. **ARP** — Resolves IP addresses to physical MAC addresses on the local network.
5. **ICMP** — Used for ping requests/replies for connectivity checks.

## Summary
- Total packets captured: 6152
- Observed both application-level protocols (HTTP, DNS) and lower-level protocols (TCP, ARP, ICMP).
- DNS lookups occur before HTTP connections.
- ARP packets are used locally for device address resolution.
- ICMP packets confirm network connectivity.

## Screenshots
1. HTTP
<img width="1920" height="945" alt="http" src="https://github.com/user-attachments/assets/9646b7fc-86b8-43f1-9c41-3b922217d1c1" />
2. DNS
<img width="1920" height="945" alt="dns" src="https://github.com/user-attachments/assets/f16d32c8-5099-49ed-a223-07a93a60e8b2" />
3. TCP
<img width="1920" height="945" alt="tcp" src="https://github.com/user-attachments/assets/5034e161-a813-4581-b02e-e1b8d5f8a831" />
4. ICMP
<img width="1920" height="945" alt="icmp" src="https://github.com/user-attachments/assets/eb78bb26-02ba-4390-925c-be3368336a64" />
5. ARP
<img width="1920" height="945" alt="arp" src="https://github.com/user-attachments/assets/1457c497-d32b-4c1f-ba81-08553296c97c" />
