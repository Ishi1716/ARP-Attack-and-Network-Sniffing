# ARP-Attack-and-Network-Sniffing
# Explore Network Sniffing and ARP Attacks

# AIM:

To explore network sniffing and ARP Attacks

## STEPS:

- `Step 1:` Install kali linux either in partition or virtual box or in live mode
- `Step 2:` Investigate on the various categories of tools as follows.
-  `Step 3:` Open terminal and try execute some kali linux commands

## ARP Attacks:  
ARP spoofing: A hacker sends fake ARP packets that link an attacker's MAC address with an IP of a computer already on the LAN. 

```
arpspoof -i eth0 -t <victim_IP> <gateway_IP>
```
## Tools Commonly Used:

**ARP Spoofing:** arpspoof, ettercap, bettercap

**Sniffing:** wireshark, tcpdump, dsniff
## Architecture Diagram
```
                     +-------------------+
                     |   Attacker (Kali) |
                     |  [ARP Spoof Tool] |
                     +---------+---------+
                               |
               +---------------+----------------+
               |                                |
       +-------v-------+              +---------v--------+
       | Victim Device |              | Gateway/Router   |
       | (e.g., Laptop)|              | (Default Gateway)|
       +---------------+              +------------------+
               |                                |
       ====== Normal ARP Traffic ===============|
               |                                |
               +---------> Internet             |
                         (DNS, HTTP, etc.)      |
                                                |
                  [Start ARP Spoofing/Poisoning]
                               |
                               v
               +-------------------------------+
               |  Attacker becomes MITM        |
               | (Man-in-the-Middle via ARP)   |
               +-------------------------------+
                               |
                     [Sniff Packets Using]
                 e.g., Wireshark, tcpdump, Ettercap

         +----------------------------------------------+
         | Captured Info:                               |
         |  - IP Addresses                              |
         |  - DNS Requests                              |
         |  - HTTP/HTTPS Data (if not encrypted)        |
         |  - Credentials (if sent in plain text)       |
         +----------------------------------------------+

```
## OUTPUT:

## arp -a

<img width="800" height="600" alt="exp 4" src="https://github.com/user-attachments/assets/c901286f-b2e7-4c9b-9838-9afb13f61dff" />


## arpspoof -i eth0 -t <victim_IP> <gateway_IP>


<img width="901" height="884" alt="image" src="https://github.com/user-attachments/assets/b42383b8-1eea-4677-a395-f5d987c78f70" />

## DSNIFF

<img width="707" height="133" alt="image" src="https://github.com/user-attachments/assets/7a6cd25e-ebad-4a91-9dcf-8e914e3eb2c1" />




## RESULT:
The kali linux tools for ARP Attack and Network Sniffing were identified successfully
