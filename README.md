

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
https://www.ietf.org/archive/id/draft-reilly-rem-protocol-00.html

Zenodo
https://zenodo.org/

OpenTimestamps
https://opentimestamps.org/

# BRAND.md — REM (Reilly EternaMark)

## Canonical name
**Reilly EternaMark (REM)**

Use the full name on first mention. The short form **REM** is acceptable thereafter.

## One-line tagline
REM — ledger-agnostic permanence: blockchain timestamping + DOI registration for verifiable, citable artifacts.

## Canonical references
- IETF Internet-Draft: *Reilly EternaMark (REM) Protocol* — draft-reilly-rem-protocol-00. DOI snapshot: `https://zenodo.org/records/17185285` (use this DOI when citing).
- GitHub (canonical repo): `https://github.com/lawrencejohnreilly-creator/rem-protocol`
- Contact / maintainer: Lawrence John Reilly — lawrencejohnreilly@gmail.com

## How to cite (recommended)
Reilly, L. J. (2025). REM (Reilly EternaMark) — DOI: 10.xxxx/rem.xxxxx — IETF Internet-Draft: draft-reilly-rem-protocol-00. Archived and timestamped (Zenodo + OpenTimestamps).

## Recommended usage rules
- Capitalization: use **Reilly EternaMark** on formal documents and **REM** for short references.
- Do not use only the token `rem` in contexts where it could be ambiguous (e.g., repo names or package names) — prefer `rem-protocol` or `reilly-eternamark`.
- Add the DOI and OTS proof references to any release notes or publication metadata.

## Visual / assets
- Logo: (placeholder) `logo.svg` — add when available.
- Colors / fonts: TBD — keep a clean, minimal aesthetic for docs.

## Handles & naming guidance (suggestions)
- GitHub repo: `lawrencejohnreilly-creator/rem-protocol` (current) — consider creating a `rem-protocol` organization for governance if project grows.
- Domain (optional): `reillyeternamark.org` or `rem-protocol.org` (reserve if you want independent landing page).
- Social/X handle: consider `@REMprotocol` or `@ReillyEMark` (check availability before committing).

## License & contribution
- Default to MIT for demo artifacts; include `LICENSE` at repo root.
- Add `CONTRIBUTING.md` with short notes: how to open issues, PR conventions, contact for sketches.

## Quick verification note
Include a short verification recipe in docs:
1. Download DOI archive (PDF).  
2. Verify SHA256 hash matches `sha256:...` in draft appendix.  
3. Verify OpenTimestamps proof (`ots verify REM_package.pdf`).  
4. Verify DOI metadata contains anchor fields (`ledger_root`, `anchor_proof`) per REM schema.

---

(End of BRAND.md)



This README itself serves as a reference implementation: simple, transparent, and reproducible.
