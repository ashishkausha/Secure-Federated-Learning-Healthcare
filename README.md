# Security-Aware Data Offloading & Optimization in Healthcare Systems

### 📄 [Read the Full M.Tech Thesis (PDF)](./Kashish_Healthcare_Security_Thesis.pdf)

📌 Project Overview
This project presents a Secure Federated Learning (FL) Framework designed for healthcare environments. It addresses the challenges of handling sensitive patient data by implementing a dynamic offloading strategy across a Cloud-Edge-Fog continuum.

The system intelligently classifies healthcare data (e.g., Critical Patient Data vs. Research Data) and routes it to the optimal processing node (Edge, Fog, or Cloud) based on sensitivity, delay tolerance, and task size.

🚀 Key Features
Dynamic Task Offloading: Algorithms to assign tasks to Edge, Fog, or Cloud nodes to minimize latency and cost.

Data Classification Engine: Sorts data into 6 categories (e.g., Critical, Operational, Archival) to ensure sensitive data never leaves the local Edge nodes.

Security & Integrity: Implements Merkle Tree Hashing to verify the integrity of model updates and prevent tampering during the Federated Learning process.

Load Balancing: Uses Docker containers to migrate tasks from overloaded nodes to underloaded ones dynamically.

🛠️ Tech Stack
Languages: Python (Scheduler logic & data processing)

Orchestration: Kubernetes (K8s) & Kind (Kubernetes-in-Docker)

Containerization: Docker Desktop

Scripting: Bash (Automation of cluster setup)

Environment: Ubuntu WSL2

📊 Performance Results
The proposed framework was tested against standard baselines (Random Node Selector, Edge-Heavy Method, and ELBO). Results demonstrated:

31.5% reduction in Total Execution Time compared to Edge-Heavy approaches.

Significant throughput improvement, achieving 10.8 workflows/unit time compared to 6.5 in baseline methods.

Cost Efficiency: maintained the lowest cost profile across all workload categories.

🏗️ Architecture
The system operates on a three-tier architecture:

Edge Nodes: Located at hospitals (low latency, high privacy) for Critical Patient Data.

Fog Nodes: Intermediate layer for aggregation and Operational Data.

Cloud Node: Centralized server for archival storage and global model updates.


---
*This project was submitted as a Master of Engineering Thesis at Thapar Institute of Engineering & Technology.*
