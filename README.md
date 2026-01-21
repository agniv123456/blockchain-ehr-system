# blockchain-ehr-system
A secure, decentralized, and patient-centric Electronic Health Record (EHR) system powered by blockchain technology to ensure data privacy, integrity, and seamless data sharing across hospitals and healthcare providers.

📌 Table of Contents

Problem Statement

Proposed Solution

Key Features

System Architecture

Workflow

Tech Stack

Repository Structure

Smart Contract Overview

Security & Privacy

Installation & Setup

Demo Flow

Use Cases

Future Enhancements

Team

License

❗ Problem Statement

Current Electronic Health Record (EHR) systems face several critical challenges:

Centralized data storage vulnerable to breaches

Limited interoperability between hospitals

Lack of patient ownership and control

Unauthorized access and data tampering

Inefficient record sharing during emergencies

These issues compromise patient privacy, data security, and healthcare efficiency.

💡 Proposed Solution

We propose a Blockchain-powered EHR system that:

Gives patients full ownership of their medical data

Stores medical records securely using IPFS (off-chain)

Stores record references (hashes) immutably on the blockchain

Enables consent-based data sharing between hospitals

Maintains a transparent audit trail of all access events

✨ Key Features

🔐 Patient-controlled access management

🧾 Immutable and tamper-proof medical records

🔑 Role-Based Access Control (RBAC)

🔄 Interoperable data sharing across hospitals

📦 Off-chain encrypted storage using IPFS

🕵️ Complete auditability of data access

🧑‍⚕️ Hospital & doctor authorization via smart contracts

🏗️ System Architecture

High-level architecture:

Patient / Hospital
       |
       v
Frontend (React + MetaMask)
       |
       v
Backend (API Layer)
       |
       +----> IPFS (Medical Records)
       |
       +----> Blockchain (Ethereum / Polygon)

Components:

Frontend: User interface for patients and hospitals

Backend: Handles IPFS uploads and blockchain interactions

Blockchain: Stores hashes, permissions, and access logs

IPFS: Stores encrypted medical documents

🔄 Workflow

Patient uploads a medical document

Document is encrypted and stored on IPFS

IPFS hash is stored on blockchain via smart contract

Patient grants access to a hospital/doctor

Authorized hospital retrieves IPFS hash from blockchain

Medical record is accessed securely from IPFS

🛠️ Tech Stack
Layer	Technology
Blockchain	Ethereum / Polygon
Smart Contracts	Solidity
Storage	IPFS
Backend	Flask / Node.js
Frontend	React.js
Wallet	MetaMask
Cryptography	Public-Private Key Encryption
📂 Repository Structure
blockchain-ehr-system/
│
├── smart-contracts/     # Solidity smart contracts
├── backend/             # Backend APIs & blockchain interaction
├── frontend/            # React frontend
├── ipfs/                # IPFS upload utilities
├── docs/                # Documentation
├── architecture/        # System diagrams
├── demo/                # Screenshots & demo assets
└── README.md

📜 Smart Contract Overview
Core Functionalities:

Store IPFS hashes of medical records

Grant and revoke access permissions

Verify authorized access

Maintain immutable record history

Sample Contract Logic:

addRecord(ipfsHash)

grantAccess(hospitalAddress)

revokeAccess(hospitalAddress)

getRecords(patientAddress)

🔐 Security & Privacy

Medical data never stored directly on blockchain

Records stored encrypted on IPFS

Blockchain stores only hash references

Access controlled via smart contracts

Every access is logged and auditable

Eliminates single point of failure

⚙️ Installation & Setup (Prototype)
Prerequisites

Node.js / Python

MetaMask wallet

Ganache / Polygon Testnet

IPFS (local or Infura)

Steps
# Clone repository
git clone https://github.com/agniv123456/blockchain-ehr-system.git

# Install backend dependencies
cd backend
pip install -r requirements.txt

# Run backend server
python app.py

🎥 Demo Flow (For Hackathon)

Patient logs in using MetaMask

Uploads a medical record

File stored on IPFS

IPFS hash recorded on blockchain

Patient grants hospital access

Hospital retrieves and views record

Access log visible on-chain

⏱️ Total demo time: ~2 minutes

🧪 Use Cases

Hospital-to-hospital record sharing

Emergency access to patient history

Long-term medical record preservation

Insurance claim verification

Cross-border healthcare access

🔮 Future Enhancements

Zero-Knowledge Proofs (ZKP) for privacy

AI-based medical analytics

Emergency override with multi-signature approval

Integration with wearable devices

Government & insurance authority access

Mobile application support

👥 Team

Agniv Banerjee

Team Members (Hackathon)

📜 License

This project is licensed under the MIT License — free to use, modify, and distribute.

⭐ Final Note (For Judges)

This project demonstrates how blockchain can transform healthcare by placing patients at the center of data ownership while enabling secure, transparent, and interoperable medical record sharing.
