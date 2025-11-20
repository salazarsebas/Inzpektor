# 🕵️‍♂️ Inzpektor  
### Zero-Knowledge Clean Hands + On-Chain Reputation for Stellar

Inzpektor is a **privacy-preserving verification layer** built on Stellar/Soroban that enables wallets, apps, and institutions to verify user integrity **without revealing personal data**.

Inspired by zero-knowledge identity systems like *Proof of Clean Hands*, Inzpektor introduces:

- ✔ ZK-based Clean Hands Credentials  
- ✔ On-chain attestation verification  
- ✔ Reputation scoring for wallets  
- ✔ Compliance without surveillance  

---

## 🚀 Project Overview

**Inzpektor** brings a new security primitive to Stellar:  
a **ZK-Clean Hands Credential** that proves a user is legitimate *without exposing who they are*.

Users generate a **zero-knowledge proof** that demonstrates:

- they passed an identity screening  
- they are not on sanctions or risk lists  
- they control the wallet they claim  
- they reveal **zero personal data**  

A Soroban contract verifies the attestation and stores a hashed credential.  
From there, Inzpektor tracks **on-chain reputation** to measure trustworthiness over time.

---

## 🔐 ZK-Clean Hands Verification

### ✨ Purpose  
Before interacting with Stellar apps, users mint a **CleanHands Credential**.

### 🧠 The user proves (in ZK):  
- Passed an identity / compliance check  
- Not present on any sanctions/risk list  
- Ownership of the wallet  
- Zero personal information leakage  

### 🛠 How it works  
1. User completes identity check off-chain (mock or real).  
2. ZK circuit generates a `zk-proof.json`.  
3. Proof is submitted to the **CleanHandsVerifier** Soroban contract.  
4. Contract verifies → stores **attestation hash**.  
5. User receives a **CleanHands Credential** linked to their wallet.

This serves as a **privacy-preserving trust badge** for the network.

---

## ⭐ On-Chain Reputation

Every wallet interacting with Inzpektor receives a **dynamic reputation score**.

### 🧾 Reputation increases with:  
- CleanHands credential verification  
- Clean transaction history  
- Zero interactions with flagged addresses  
- Voluntary proof refresh cycles  

### 🚫 Reputation decreases with:  
- Failed verification attempts  
- Transactions with high-risk wallets  
- Expired or revoked credentials
