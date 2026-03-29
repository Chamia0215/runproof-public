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


## Quick links (Public surface)

- Pages top: https://runproof-chamia.pages.dev/
- Verify Portal: https://runproof-chamia.pages.dev/portal/
- Browser Playground: https://runproof-chamia.pages.dev/playground/
- Docs: https://runproof-chamia.pages.dev/docs/
- Adoption guide: https://runproof-chamia.pages.dev/docs/adoption.htm
- Performance guide: https://runproof-chamia.pages.dev/docs/performance.htm
- FAQ: https://runproof-chamia.pages.dev/docs/faq.htm
- Flow: https://runproof-chamia.pages.dev/docs/flow.htm
- Operations: https://runproof-chamia.pages.dev/docs/ops.htm
- API entry: https://runproof-chamia.pages.dev/api/
- Business page: https://runproof-chamia.pages.dev/business-index.htm
- API Reference: https://runproof-chamia.pages.dev/ref/api_reference_v0.1.1.md
- OpenAPI: https://runproof-chamia.pages.dev/ref/openapi.yaml
- Freeze statement: https://runproof-chamia.pages.dev/freeze/freeze_v2.md
- Data Input Policy: https://runproof-chamia.pages.dev/policy/data_input_policy_v1.md
- API Base (Workers): https://runproof.chamia-20260215.workers.dev
- Public releases (evidence assets): https://github.com/Chamia0215/runproof-public/releases

## Performance snapshot (2026-03-29)

Reference measurements over the public internet (Japan, Windows PowerShell 7.5.5, sequential runs):

- POST /v1/verify: avg 1427.07 ms, p95 1654.70 ms
- POST /v1/receipts: avg 1600.06 ms, p95 2118.52 ms
- Sequential runs: verify ~42.03 req/min, receipts ~37.43 req/min
- Details: https://runproof-chamia.pages.dev/docs/performance.htm

## Public repo role

This public repo is the **public shelf / discovery surface** for RunProof.
Current public guidance lives on the Pages site above. The development repo remains non-public.

日本語：この public repo は **公開棚 / 発見導線** です。
現在の説明と導線の正本は Pages 側にあります。開発用リポジトリは非公開です。

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
This README is intentionally minimal.

- Start with meaning and public guidance: https://runproof-chamia.pages.dev/docs/
- Try issuing with a key: https://runproof-chamia.pages.dev/playground/
- Check a receipt in the browser: https://runproof-chamia.pages.dev/portal/

日本語：この README は最小構成です。

- まず意味と公開導線を見る → https://runproof-chamia.pages.dev/docs/
- API 発行を試す → https://runproof-chamia.pages.dev/playground/
- receipt の結果を確認する → https://runproof-chamia.pages.dev/portal/
