# 🧭 Chord Protocol - Distributed Hash Table (DHT) Implementation

This project implements the **Chord Protocol**, a scalable and decentralized DHT-based system used in peer-to-peer networks. The design ensures efficient data lookup, insertion, deletion, and node join operations across a distributed ring topology.

## 📁 Repository Structure

```
Group_5/
│
├── docs/                     # Project documentation
│   └── Project_Report.pdf
│
├── src/                      # Source code
│   ├── Node_DHT.py           # Core DHT Node implementation
│   └── Client.py             # Client interface for interacting with the ring
│
├── screenshots/              # Step-by-step demo screenshots
├── run_instructions.txt      # Setup and execution guide
└── README.md                 # Project overview
```

## 🔧 Features

- Implements a **ring-based DHT** using the Chord protocol.
- SHA-1 based consistent hashing for node and key placement.
- Efficient finger table construction to reduce lookup time to **O(log N)**.
- Support for:
  - Creating a new ring
  - Dynamically joining new nodes
  - Inserting, searching, and deleting key-value pairs
- Console-based client interface

## 🧠 Concepts Demonstrated

- Distributed systems and peer-to-peer architecture
- Finger table-based routing
- Hashing and consistent key assignment
- Node failure resilience (partial)

## 🚀 Getting Started

### ✅ Prerequisites

- Python 3
- Ubuntu environment (native/WSL/VM)

```bash
sudo apt update
sudo apt install python3
```

### ▶️ Run Instructions

```bash
# Step 1: Create the ring (use a base port like 8000)
python3 Node_DHT.py 8000

# Step 2: Join a new node to the existing ring
# Syntax: python3 Node_DHT.py <new_node_port> <existing_node_port>
python3 Node_DHT.py 8001 8000
python3 Node_DHT.py 8002 8000

# Step 3: Launch the client to interact with the DHT
python3 Client.py
# Provide the port number (e.g., 8000) to interact with a particular node
```

### 📸 Screenshots

Images available under `/screenshots` show:

- Ring creation
- Node joining
- Finger table propagation
- Key insertions and lookups

## 📂 Code Overview

### 🧩 `Node_DHT.py`

- Implements the core DHT functionality
- Maintains finger tables and data store
- Manages communication with other nodes over sockets
- Handles key-value storage and lookup

### 💬 `Client.py`

- Simple command-line interface for end-users
- Allows inserting, deleting, and viewing key-value entries on any node

## 📜 Report

Detailed documentation is available in [`docs/Project_Report.pdf`](docs/Project_Report.pdf) explaining the algorithm design, assumptions, and implementation challenges.

## 🤝 Contributors

- Group 5 — M.Tech ICT Students
- Project under: **[DAU - Prof. Amit Mankodi]**

## 🪪 License

This project is intended for educational and academic purposes.
