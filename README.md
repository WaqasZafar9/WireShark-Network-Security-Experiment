# WireShark-Network-Security-Experiment
This repository documents a network security experiment conducted using Wireshark. The primary objectives include capturing and analyzing network traffic during interactions with Facebook and YouTube.
# Network Security Experiment Repository

## Experiment Description

### Capture File Properties

#### Facebook Capture
- **Name:** 
- **Length:** 18 MB

- **Format:** Wireshark/... - pcapng
- **Encapsulation:** Ethernet
- **Time:**
  - First packet: 2024-01-07 15:49:33
  - Last packet: 2024-01-07 16:23:33
  - Elapsed: 00:34:00
- **Application:** Dumpcap (Wireshark) 4.2.0 (v4.2.0-0-g54eedfc63953)
- **Interfaces:**
  - Wi-Fi
    - Dropped packets: 0 (0.0%)
    - Capture filter: none
    - Link type: Ethernet
    - Packet size limit (snaplen): 262144 bytes
- **Statistics:**
  - Packets: 28321 captured and displayed (100.0%)
  - Time span: 2040.020 seconds
  - Average pps: 13.9
  - Average packet size: 634 bytes
  - Bytes: 17946836 (100.0%)
  - Average bytes/s: 8797
  - Average bits/s: 70 k

#### YouTube Capture
- **Name:** `
- **Length:** 219 MB

- **Format:** Wireshark/... - pcapng
- **Encapsulation:** Ethernet
- **Time:**
  - First packet: 2024-01-08 20:31:07
  - Last packet: 2024-01-08 21:02:26
  - Elapsed: 00:31:18

- **Application:** Dumpcap (Wireshark) 4.2.0 (v4.2.0-0-g54eedfc63953)
- **Interfaces:**
  - Wi-Fi
    - Dropped packets: 0 (0.0%)
    - Capture filter: none
    - Link type: Ethernet
    - Packet size limit (snaplen): 262144 bytes
- **Statistics:**
  - Packets: 208212 captured and displayed (100.0%)
  - Time span: 1878.976 seconds
  - Average pps: 110.8
  - Average packet size: 1020 bytes
  - Bytes: 212411107 (100.0%)
  - Average bytes/s: 113 k
  - Average bits/s: 904 k

### Display Filter Expressions:

#### Facebook Filters
1. **HTTP Packets:**
   - Filter: `http`
   - Total displayed: 4 packets

2. **SSL Packets:**
   - Filter: `ip.addr == 157.240.227.56 and ssl`
   - Displayed: 123 bytes (0.4%)

3. **TCP Packets - HTTP Subset:**
   - Displayed: 25 bytes (0.1%)
   - Filter: `tcp.port == 80`

#### YouTube Filters
1. **HTTP Protocol Filter:**
   - Filter: `tcp.dstport == 80`
   - Total displayed: 208212 packets (100.0%)

2. **TCP Traffic to/from YouTube Servers:**
   - Filter: `tcp.port == 443 and ip.addr == 142.250.181.78`
   - Displayed: 10 packets

3. **TCP Traffic from Computer to YouTube Servers:**
   - Filter: `ip.src == 192.168.181.113 and ip.dst == 142.250.181.78`
   - Displayed: 1958 packets (0.9%)

4. **TCP Traffic from YouTube Servers to Computer:**
   - Filter: `ip.src == 142.250.181.78 and ip.dst == 192.168.181.113`
   - Displayed: 5762 packets (2.8%)

### Flags Analysis:

#### Facebook Flags
- **SYN Flag:**
  - Displayed: 4 packets (0.0%)

- **PUSH Flag:**
  - Displayed: 144 packets (0.5%)

- **Reset Flag:**
  - Displayed: 0 packets

#### YouTube Flags
- **SYN Flag:**
  - Displayed: 10 packets (0.0%)

- **PUSH Flag:**
  - Displayed: 36748 packets (17.6%)

- **Reset Flag:**
  - Displayed: 149 packets (0.1%)

### Reference Videos
- [YouTube Video 1](https://youtu.be/u4ht-E-Kihk?si=4SBxFQ9y8TPN8S9e)
- [YouTube Video 2](https://youtu.be/5qecyZHL-GU?si=89GhFkp3VLl0bHWZ)



