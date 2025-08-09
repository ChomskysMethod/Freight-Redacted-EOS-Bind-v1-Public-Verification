# Freight Redacted EOS Bind v1 — Public Verification

This repository contains the final **public verification bundle** for the Freight Redacted EOS Bind v1 release.

## Canonical Master Hash

```
3b67128f34b240d94256fc129a0c701be61d4f4e3afe59570287fe9bcd558932c3dd63287986e82b9aaf19da65ba00e202b2e42c285c6f5f1a58845608eebbbc
```

*(Full hash present in the Chain-of-Custody file.)*

## Contents of the Bundle

- **Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.txt** — Full cryptographic audit trail.
- **Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.sig** — Ed25519 detached signature.
- **Freight_Jenna_Ed25519_public.pem** — Public verification key.
- **Freight_Redacted_EOS_Bind_v1_Public_Upload_Sheet.docx** — Human-readable release context.
- **Verification Card (PDF/PNG)** — Quick visual reference for verification.

## Verification Instructions

1. Obtain the public key (`Freight_Jenna_Ed25519_public.pem`).
2. Use an Ed25519 verification tool (e.g., `openssl`, `python-ed25519`) to verify:
   ```
   openssl dgst -verify Freight_Jenna_Ed25519_public.pem                 -keyform PEM                 -sha512                 -signature Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.sig                 Freight_Redacted_EOS_Bind_v1_Chain_of_Custody.txt
   ```
3. Confirm the computed hash from the Chain-of-Custody file matches the **Canonical Master Hash** above.
4. (Optional) Compare with the Verification Card for a quick visual match.

## License

This release is provided for public verification purposes. Redistribution of this bundle in full is permitted.
