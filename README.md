# rem-protocol
Reference implementation of the REM Protocol (DOI + Blockchain Permanence) – Internet-Draft draft-reilly-rem-protocol-00
# REM Protocol Reference Implementation (Proof-of-Concept)

This repository provides a minimal demonstration of the **Reilly EternaMark (REM) Protocol**, an Internet-Draft submitted to the IETF:  
🔗 [draft-reilly-rem-protocol-00](https://www.ietf.org/archive/id/draft-reilly-rem-protocol-00.html)

---

## 📌 What is REM Protocol?  
REM defines a dual-layer method for **digital permanence**:  

- **Blockchain timestamping** → immutability  
- **DOI assignment** → discoverability and persistence  

Unlike most Internet-Drafts that use placeholders, REM includes **live artifacts** (real DOIs, blockchain TXIDs, and SHA-256 hashes) that can be verified today.

---

## 🛠️ Proof-of-Concept Workflow  

1. **Upload to Zenodo**  
   - Deposit a document or dataset.  
   - Zenodo mints a permanent **DOI**.  

2. **Generate a SHA-256 hash**  
   ```bash
   shasum -a 256 mydocument.pdf
3. Timestamp with OpenTimestamps
   ots stamp mydocument.pdf
   ots info mydocument.ots
Produces a blockchain transaction ID (TXID) on Bitcoin.

4. Record the Pair

Combine the DOI + TXID + SHA-256 hash as a dual-layer permanence record.

Example Proof Artifact
{
  "sha256": "02439f01ba0b805ba3011aaeb2783ffb096c1c6ad847876e75d7d8b6c5c40d9b",
  "doi": "10.5281/zenodo.17096230",
  "txid": "Bitcoin block 914168 (attesting existence as of 2025-09-10 EST)"
}

Why This Matters

Verifiable today: anyone can check the DOI and TXID independently.

Immutable + discoverable: permanence guaranteed by blockchain + scholarly infrastructure.

Reference implementation: small, reproducible steps that prove the REM Protocol works.

🔗 References

IETF Internet-Draft: REM Protocol
https://www.ietf.org/archive/id/draft-reilly-rem-protocol-00.html?utm_source=chatgpt.com

Zenodo
https://zenodo.org/

OpenTimestamps
https://opentimestamps.org/

This README itself serves as a reference implementation: simple, transparent, and reproducible.
