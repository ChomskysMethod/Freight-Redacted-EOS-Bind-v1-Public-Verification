# Freight–[Redacted] EOS Bind v1.0 — Public Verification Bundle

## Contents of the Bundle

- **Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.txt** — Full cryptographic audit trail.  
- **Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.sig** — Ed25519 detached signature.  
- **Freight_Redacted_Ed25519_public.pem** — Public verification key.  
- **Freight_Redacted_EOS_Bind_v1_Public_Upload_Sheet.docx** — Human-readable release context.  
- **Verification Card (PDF/PNG)** — Quick visual reference for verification.

## Verification Instructions

1. Obtain the public key (`Freight_Redacted_Ed25519_public.pem`).
2. Use an Ed25519 verification tool (e.g., `openssl`, `python-ed25519`) to verify:
   
   ```bash
   openssl dgst -verify Freight_Redacted_Ed25519_public.pem -signature Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.sig Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.txt
