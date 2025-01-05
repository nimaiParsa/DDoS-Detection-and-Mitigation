# DDoS Detection and Mitigation using Statistical Approaches

## Overview
This project is designed to detect and mitigate DDoS (Distributed Denial of Service) attacks using statistical techniques, specifically chi-square tests and entropy measures. The system aims to distinguish between legitimate and malicious traffic to ensure the server's availability.

## Project Setup
The project comprises a single server implementing a firewall to detect and mitigate DDoS attacks. Clients and attackers simulate requests through scripts. The server and clients must belong to the same subnet (connected to a common access point or hotspot) for demonstration purposes. The server operates on an IP dynamically allocated on the subnet, with clients sending messages to that IP.

---

## Instructions for Setup and Demonstration

### 1. Start the Server
Run the server script:
```bash
python3 server.py
```

### 2. Set Up the Firewall
In a separate terminal, execute the firewall script with administrative privileges:
```bash
sudo python3 firewall.py
```

At this point, both the server and the firewall will be operational.

### 3. Simulate Clients
The following client scripts generate different types of traffic:

#### Normal Client Traffic
- **File:** `client_normal.py`
- **Description:** This script generates normal traffic to the server, sending packets with randomized delays between transmissions using `sleep`.

#### Attacker Traffic
- **File:** `client_attacker.py`
- **Description:** This script simulates a DDoS attack by continuously sending packets to the server without any delay.

### 4. Multiple Clients from a Single Device
To generate traffic from multiple clients with varying IPs, virtual IP addresses are created on the network interface. This simulates multiple devices originating requests.

---

## References
- [Detection and Mitigation Techniques for DDoS](https://ieeexplore.ieee.org/document/1194894)
- [Advanced DDoS Detection with Entropy Measures](https://ieeexplore.ieee.org/document/10235131)

---

## Authors
- [Nimai Parsa](https://github.com/nimaiParsa)
- [K S Ananth](https://github.com/ksananth4424)
- [Pradyumn Kangule](https://github.com/Pradyumn1618)
- [Swapnil Bag](https://github.com/swaps805)
- [Devansh Agrawal](https://github.com/DevanshJouLe)
- [Bhavesh Chowdary](https://github.com/Bhaveshchowdary)

