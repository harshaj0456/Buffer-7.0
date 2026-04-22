
# ShadowTrace 🛡️
Backdoor Persistence & MITM Detection System

**Team Name:** Ciphera 
**Project Name:**  ShadowTrace
**Team Members:** Harsha Jadhav, Trupti Patil, Vidhisha Kulkarni, Anjali Mali  
**Competition:** Buffer 7.0  
**Theme:** Cybersecurity & Digital Defense  
**Language:** Java  

## Demo Video
https://drive.google.com/drive/folders/1vUVmyY9lrxSbW_oZiOgC_xtqXCkmMB0D?usp=sharing

## Problem Statement
Modern cyberattacks are becoming increasingly advanced and often remain undetected by traditional security tools.
This project mainly focuses on detecting two dangerous attacks:

1. **Backdoor Persistence Attack**  
   In this attack, malware creates hidden scheduled tasks, registry keys, and rogue processes that reinstall each other even after system cleanup.

2. **MITM (Man-In-The-Middle) Attack**  
   In this attack, the attacker silently inserts themselves between two devices and intercepts all communication without the devices knowing.

These attacks are dangerous because they allow permanent system access and silent data theft.

## Solution
ShadowTrace is a cybersecurity detection system built in Java that detects both MITM and persistence attacks using graph-based algorithms and data structures.

### Features:
1. Detects MITM attacks using ARP cache monitoring and path deviation analysis.
2. Detects hidden persistence cycles using graph traversal algorithms.
3. Simulates infection spread across the network.
4. Scores threats based on severity and risk level.
5. Generates a safe removal plan to prevent malware reinstallation.
6. Produces a complete incident report with timeline and findings.
7. Includes both console-based simulation and web dashboard.

## Data Structures Used
1. **Weighted Graph (Adjacency List)**  
   Used for network topology and node communication mapping.
2. **HashMap**  
   Used for ARP cache monitoring and fast IP-MAC lookup.
3. **Priority Queue / Max Heap**  
   Used for risk-based threat scoring.
4. **Stack**  
   Used internally in Tarjan SCC algorithm.
5. **Queue (BFS)**  
   Used for infection spread simulation.
6. **Bloom Filter**  
   Used to avoid duplicate node processing.
7. **Union-Find (DSU)**  
   Used for compromised vs clean node segmentation.

## Algorithms Used
1. **Dijkstra's Algorithm**  
   Used for shortest safe path detection.
2. **Tarjan SCC Algorithm**  
   Used for persistence cycle detection.
3. **Articulation Point Detection**  
   Used to find critical system nodes.
4. **Betweenness Centrality**  
   Used to detect likely entry point.
5. **BFS Traversal**  
   Used for attack spread simulation.
6. **Topological Sort**  
   Used for safe malware removal ordering.

## Web Dashboard
The project also includes a web dashboard using:
- Java Spring Boot
- HTML, CSS, JavaScript
- Chart.js and D3.js
- It connects to the backend via REST APIs and displays detection results visually.

The dashboard visually shows:
- compromised nodes
- clean nodes
- threat score
- spread simulation
- removal plan
- custom simulation

## Output
The system generates:
- threat events
- infection timeline
- clean node list
- compromised node list
- safe removal steps
- final incident report

## Note
This project was built for **Buffer 7.0 Hackathon** under the **Cybersecurity & Digital Defense** theme.
All algorithms are implemented from scratch in Java without using external graph libraries.

**Built with Java | Team Ciphera | ShadowTrace**
