rem_demo/README.md
This directory contains the demonstration artifacts for the **Reilly EternaMark (REM) Protocol)** — a dual‑layer permanence method combining DOI archiving with blockchain timestamping.


## Files
- **REM_package.pdf** – Self‑contained explainer/whitepaper bundle
- **REM_package.pdf.ots** – (Optional) OpenTimestamps proof
- **BRAND.md** – Lightweight visual guidance for screenshots, badges, and one‑liners
- **CITE.md** – How to cite the REM Protocol (DOI + TxID) and reference the Internet‑Draft
- **CHANGELOG.md** – Notable public changes


## Verify Permanence
1. Resolve DOI: `<PASTE_DOI_URL_HERE>`
2. Verify OTS: `ots verify REM_package.pdf.ots` (or via opentimestamps.org)
3. Match SHA‑256 of PDF: `sha256sum REM_package.pdf`
4. Confirm TxID on chain: `<PASTE_BLOCK_EXPLORER_TXID_LINK_HERE>`


## License
See `LICENSE` (MIT recommended for the demo pack).
