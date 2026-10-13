# Klisten ToolGuard — limited beta

This connector exposes `toolguard_gate_check_paid` and `toolguard_attestation_get` on the existing hosted service. It does not register target tools, create scans, execute tools, or guarantee safety.

## Customer setup and payment
1. Sign in at https://klisten.co.kr/app using your own account.
2. Follow https://klisten.co.kr/customer-guide to register your authorized tool and policy, complete the prerequisite Scan and baseline approval.
3. Issue your own least-privilege key: gate:check and/or attestations:read. Set a spending limit. Never paste keys into conversations or repositories.
4. ToolGuard uses the existing prepaid wallet: $5 PayPal Live top-up, Scan $0.05, Gate $0.001. No new subscription is introduced. A payment success screen alone is not proof of credited balance. Confirm credit before retrying a payment.
5. Configure the customer key securely in your host. Use the actual tools/list schema. Gate results are policy decisions, not execution permission. Do not retry a paid call with a new idempotency key after an uncertain response.

## Limits and support
This package itself does not collect payment. Only authorized service calls may debit the Klisten wallet. No shared reviewer/admin key is included. Free catalog lookup is not a paid Gate.
Support: klisteninc@gmail.com. Privacy: https://klisten.co.kr/privacy.html . Terms: https://klisten.co.kr/terms.html .

## Validation status
Configuration prepared; native host install and authenticated paid-path use have NOT been newly validated in this expansion task. Historical service tests do not establish this host's compatibility. Authenticated MCP discovery and an existing attestation read passed against the hosted service. Native Cursor installation and conversation calls remain unverified.

## Cursor setup
Use the plugin configuration UI to provide KLISTEN_API_KEY. Native Cursor installation and conversation tests remain pending. On October 12, 2026 the Cursor Marketplace Team confirmed by email that the described free integration with an externally billed hosted API works under its terms. This confirmation is not marketplace approval. Remove only this plugin to uninstall; revoke its key separately in Klisten if no longer used.

## Who this is for
For developers adding an evidence and policy-check step around registered MCP tools. Read an existing attestation first; request a paid Gate decision only after preparing your target, policy, scan and baseline. Your application must enforce the verified result. ToolGuard does not execute tools or guarantee security.

## Setup and usage pricing
The integration package is free to install. Hosted API usage is separate: Scan $0.05 and Gate $0.001, using the existing prepaid wallet. Check compatibility and prerequisites before the $5 PayPal top-up. Set a spending limit and never put credentials in chat or public code.
Start here: https://klisten.co.kr/toolguard-start
Customer guide: https://klisten.co.kr/customer-guide
Support: klisteninc@gmail.com
