# Security-Aware Data Offloading & Optimization in Healthcare Systems

### 📄 [Read the Full M.Tech Thesis (PDF)](./MTech_Thesis_Final.pdf)

## 📌 Project Overview
This project presents a **Secure Federated Learning (FL) Framework** designed for healthcare environments. [cite_start]It addresses the challenges of handling sensitive patient data by implementing a dynamic offloading strategy across a **Cloud-Edge-Fog continuum**[cite: 38, 42].

[cite_start]The system intelligently classifies healthcare data (e.g., Critical Patient Data vs. Research Data) and routes it to the optimal processing node (Edge, Fog, or Cloud) based on sensitivity, delay tolerance, and task size[cite: 393, 440].

## 🚀 Key Features
* [cite_start]**Dynamic Task Offloading:** Algorithms to assign tasks to Edge, Fog, or Cloud nodes to minimize latency and cost[cite: 464, 467].
* [cite_start]**Data Classification Engine:** Sorts data into 6 categories (e.g., Critical, Operational, Archival) to ensure sensitive data never leaves the local Edge nodes[cite: 393].
* [cite_start]**Security & Integrity:** Implements **Merkle Tree Hashing** to verify the integrity of model updates and prevent tampering during the Federated Learning process[cite: 417, 569].
* [cite_start]**Load Balancing:** Uses Docker containers to migrate tasks from overloaded nodes to underloaded ones dynamically[cite: 554].

## 🛠️ Tech Stack
* [cite_start]**Languages:** Python (Scheduler logic & data processing) 
* [cite_start]**Orchestration:** Kubernetes (K8s) & Kind (Kubernetes-in-Docker) [cite: 664]
* [cite_start]**Containerization:** Docker Desktop 
* [cite_start]**Scripting:** Bash (Automation of cluster setup) 
* [cite_start]**Environment:** Ubuntu WSL2 [cite: 665]

## 📊 Performance Results
The proposed framework was tested against standard baselines (Random Node Selector, Edge-Heavy Method, and ELBO). Results demonstrated:
* [cite_start]**31.5% reduction** in Total Execution Time compared to Edge-Heavy approaches[cite: 794].
* [cite_start]**Significant throughput improvement**, achieving 10.8 workflows/unit time compared to 6.5 in baseline methods[cite: 853].
* [cite_start]**Cost Efficiency:** maintained the lowest cost profile across all workload categories[cite: 976].

## 🏗️ Architecture
The system operates on a three-tier architecture:
1.  [cite_start]**Edge Nodes:** Located at hospitals (low latency, high privacy) for Critical Patient Data[cite: 303].
2.  [cite_start]**Fog Nodes:** Intermediate layer for aggregation and Operational Data[cite: 318].
3.  [cite_start]**Cloud Node:** Centralized server for archival storage and global model updates[cite: 334].

---
[cite_start]*This project was submitted as a Master of Engineering Thesis at Thapar Institute of Engineering & Technology[cite: 17].*
