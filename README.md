<!-- RUNPROOF_README_BEGIN -->

# RunProof — Execution Proof API by Chamia

RunProof is a **low-output attestation** API.
It **does not store your original inputs/outputs**. It stores only:

- non-sensitive tags (supplementary fields)
- cryptographic hash (e.g., sha256:<hex>)
- signature
- chain link
- audit logs

**Do not submit PII or secrets. Send hashes only.**


## Fixed links (Public surface)

- Browser Playground: https://runproof-chamia.pages.dev/playground/
- Verify Portal: https://runproof-chamia.pages.dev/portal/
- Docs: https://runproof-chamia.pages.dev/docs/
- OpenAPI: https://runproof-chamia.pages.dev/ref/openapi.yaml
- API Base (Workers): https://runproof.chamia-20260215.workers.dev
- Public releases (evidence assets): https://github.com/Chamia0215/runproof-public/releases

## Public docs (source of truth)

- Docs (index): https://runproof-chamia.pages.dev/
- Freeze statement: https://runproof-chamia.pages.dev/freeze/freeze_v2.md
- API Reference: https://runproof-chamia.pages.dev/ref/api_reference_v0.1.1.md
- Data Input Policy: https://runproof-chamia.pages.dev/policy/data_input_policy_v1.md

## Live API entry (Workers)

- https://runproof.chamia-20260215.workers.dev/
- https://runproof.chamia-20260215.workers.dev/health
- https://runproof.chamia-20260215.workers.dev/v1/public-key

## Quick start (outline)

1. Hash your input locally: sha256:<hex>
2. Create receipt (requires API key): POST /v1/receipts
3. Verify locally using:
   - public key (GET /v1/public-key)
   - receipt (GET /v1/receipts/{receipt_id})

## Repo safety rules

- Never commit your local secrets directory (ignored by git).
- D1 stores api_key_hash only (never store raw API keys)

<!-- RUNPROOF_README_END -->

<!-- README is intentionally minimal -->
This README is intentionally minimal. The source of truth is the public docs:
- https://runproof-chamia.pages.dev/docs/

日本語：この README は最小構成です。最新の説明と導線は Pages 側の Docs を正本とします。
- https://runproof-chamia.pages.dev/docs/

