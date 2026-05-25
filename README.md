# dLocal (d-local)

dLocal (NASDAQ: DLO) is a Uruguay-headquartered emerging-markets payment infrastructure platform connecting global merchants with billions of consumers across 60+ countries in Latin America, Africa, the Middle East, and Asia. dLocal exposes a unified set of REST APIs for accepting payments (Payins) via 1,000+ local methods, disbursing funds (Payouts V3) to beneficiaries via local rails, tokenizing cards, managing marketplace sub-merchants (dLocal for Platforms), performing KYC verifications, handling chargebacks, enrolling users for recurring Pix flows, and pulling real-time exchange rates. Native iOS and Android SDKs are published as open source on GitHub.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/d-local/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=d-local)

## Tags

Payments, Payouts, EmergingMarkets, LatAm, Africa, Asia, FX, Fintech

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## Coverage Snapshot

| Dimension | Detail |
|---|---|
| HQ | Uruguay |
| Public ticker | NASDAQ: DLO |
| Founded | 2010 |
| Countries | 60+ (LatAm, Africa, Middle East, Asia) |
| Payment methods | 1,000+ |
| Reported 2025 TPV | $41B |
| Merchant clients | 760+ |

## Environments and Authentication

| API surface | Production base URL | Sandbox base URL | Auth |
|---|---|---|---|
| Payments / Refunds / Cards / Chargebacks / Enrollments / Exchange Rates / KYC | `https://api.dlocal.com` | `https://sandbox.dlocal.com` | V2-HMAC-SHA256 (X-Login, X-Trans-Key, X-Date, Authorization) |
| Payouts V3 | `https://api.dlocal.com` | `https://sandbox.dlocal.com` | OAuth2 Bearer |
| dLocal for Platforms | `https://marketplace-api.dlocal.com` | `https://marketplace-api.dlocal-sbox.com` | OAuth2 Bearer |

## APIs

### dLocal Payments API
Create, retrieve, cancel, and authorize payments using 1,000+ local payment methods including cards, Pix, UPI, M-Pesa, Boleto, OXXO, SPEI, mobile money, cash vouchers, BNPL, wallets, and QR codes.

**Human URL:** [https://docs.dlocal.com/reference/create-payment](https://docs.dlocal.com/reference/create-payment)

- [Documentation — Create A Payment](https://docs.dlocal.com/reference/create-payment)
- [Documentation — Retrieve A Payment](https://docs.dlocal.com/reference/retrieve-a-payment)
- [Getting Started — Make Payment](https://docs.dlocal.com/docs/make-payment)
- [OpenAPI](openapi/d-local-payments-api-openapi.yml)
- [JSON Schema — Payment](json-schema/payments-payment-schema.json)
- [JSON Structure — Payment](json-structure/payments-payment-structure.json)
- [Example — Create Card Payment](examples/payments-create-payment-example.json)
- [Example — Retrieve Payment](examples/payments-retrieve-payment-example.json)
- [Example — Pix Payment](examples/payments-pix-example.json)
- [Naftiko Capability — Payments](capabilities/payments-payments.yaml)

### dLocal Refunds API
Create, retrieve, and inspect refunds against prior payments. Full or partial; settled in the original payment currency.

**Human URL:** [https://docs.dlocal.com/reference/make-a-refund](https://docs.dlocal.com/reference/make-a-refund)

- [Documentation — Make A Refund](https://docs.dlocal.com/reference/make-a-refund)
- [Documentation — Refunds Guide](https://docs.dlocal.com/docs/refunds)
- [OpenAPI](openapi/d-local-refunds-api-openapi.yml)
- [JSON Schema — Refund](json-schema/refunds-refund-schema.json)
- [Example — Make Refund](examples/refunds-make-refund-example.json)
- [Naftiko Capability — Refunds](capabilities/refunds-refunds.yaml)

### dLocal Cards API
Securely tokenize cards server-side for repeat usage and recurring billing.

**Human URL:** [https://docs.dlocal.com/reference/create-a-card](https://docs.dlocal.com/reference/create-a-card)

- [Documentation — Create A Card](https://docs.dlocal.com/reference/create-a-card)
- [Documentation — Saving Cards](https://docs.dlocal.com/docs/saving-cards)
- [OpenAPI](openapi/d-local-cards-api-openapi.yml)
- [JSON Schema — Card Token](json-schema/cards-card-token-schema.json)
- [Example — Create Card](examples/cards-create-card-example.json)
- [Naftiko Capability — Cards](capabilities/cards-cards.yaml)

### dLocal Payouts V3 API
Disburse funds to beneficiaries across 60+ countries via bank transfer, instant payment, card, mobile money, and cash pick-up. Includes balance, FX quoting, hold/release, and cancel.

**Human URL:** [https://docs.dlocal.com/reference/requesting-payout-v3](https://docs.dlocal.com/reference/requesting-payout-v3)

- [Documentation — Request A Payout](https://docs.dlocal.com/reference/requesting-payout-v3)
- [Documentation — Payouts V3 Overview](https://docs.dlocal.com/docs/overview-payouts-v3)
- [Authentication — Payouts V3 Security](https://docs.dlocal.com/reference/security-payouts-v3)
- [OpenAPI](openapi/d-local-payouts-v3-api-openapi.yml)
- [JSON Schema — Payout](json-schema/payouts-v3-payout-schema.json)
- [JSON Structure — Payout](json-structure/payouts-v3-payout-structure.json)
- [Example — Request Payout](examples/payouts-v3-request-payout-example.json)
- [Example — Get Balance](examples/payouts-v3-get-balance-example.json)
- [Naftiko Capability — Payouts V3](capabilities/payouts-v3-payouts.yaml)

### dLocal For Platforms API
Onboard sub-merchant accounts, manage KYC, attach bank accounts, settle inter-account transfers, and report balances.

**Human URL:** [https://docs.dlocal.com/docs/platforms-overview](https://docs.dlocal.com/docs/platforms-overview)

- [Documentation — Platforms Overview](https://docs.dlocal.com/docs/platforms-overview)
- [Documentation — Create Account](https://docs.dlocal.com/reference/create-account-v2-platforms-1)
- [OpenAPI](openapi/d-local-platforms-api-openapi.yml)
- [JSON Schema — Account](json-schema/platforms-account-schema.json)
- [Example — Create Account](examples/platforms-create-account-example.json)
- [Naftiko Capability — Platforms Accounts](capabilities/platforms-accounts.yaml)

### dLocal KYC Verifications API
Create and manage KYC verifications across remittance, payouts-on-hold, payins-on-hold, and standalone flows. Async webhook results.

**Human URL:** [https://docs.dlocal.com/docs/kyc-verifications-overview](https://docs.dlocal.com/docs/kyc-verifications-overview)

- [Documentation — KYC Overview](https://docs.dlocal.com/docs/kyc-verifications-overview)
- [Documentation — KYC Process](https://docs.dlocal.com/docs/kyc-verifications-process)
- [Documentation — Create Verification](https://docs.dlocal.com/reference/create-verification-1)
- [OpenAPI](openapi/d-local-kyc-verifications-api-openapi.yml)
- [Example — Create Verification](examples/kyc-create-verification-example.json)
- [Naftiko Capability — KYC Verifications](capabilities/kyc-verifications.yaml)

### dLocal Chargebacks API
Retrieve chargeback details and status, simulate chargebacks in sandbox, and receive async chargeback notifications.

**Human URL:** [https://docs.dlocal.com/reference/retrieve-a-chargeback](https://docs.dlocal.com/reference/retrieve-a-chargeback)

- [Documentation — Retrieve Chargeback](https://docs.dlocal.com/reference/retrieve-a-chargeback)
- [Documentation — Chargebacks Guide](https://docs.dlocal.com/docs/chargebacks)
- [Documentation — Chargeback Categories](https://docs.dlocal.com/docs/chargeback-categories)
- [OpenAPI](openapi/d-local-chargebacks-api-openapi.yml)

### dLocal Enrollments API
Enroll payers for recurring Pix Automático, Pix Biometrics, and SmartPix transactions in Brazil.

**Human URL:** [https://docs.dlocal.com/reference/create-enrollment](https://docs.dlocal.com/reference/create-enrollment)

- [Documentation — Create Enrollment](https://docs.dlocal.com/reference/create-enrollment)
- [Documentation — Pix Automático](https://docs.dlocal.com/docs/brazil-pix-automatico)
- [Documentation — Pix Biometrics](https://docs.dlocal.com/docs/brazil-pix-biometrics)
- [Documentation — SmartPix](https://docs.dlocal.com/docs/brazil-smartpix)
- [OpenAPI](openapi/d-local-enrollments-api-openapi.yml)

### dLocal Exchange Rates API
Retrieve real-time FX rates between settlement and local currencies before creating a payment or payout.

**Human URL:** [https://docs.dlocal.com/reference/get-an-exchange-rate](https://docs.dlocal.com/reference/get-an-exchange-rate)

- [Documentation — Get Exchange Rate](https://docs.dlocal.com/reference/get-an-exchange-rate)
- [OpenAPI](openapi/d-local-exchange-rates-api-openapi.yml)
- [Example — Get Rate](examples/exchange-rates-get-rate-example.json)

## Common Resources

### Portals and Documentation
- [Portal](https://dlocal.com/)
- [Documentation](https://docs.dlocal.com/)
- [API Reference](https://docs.dlocal.com/reference/api)
- [Get Started](https://docs.dlocal.com/docs/get-started)
- [Make a Test Payment (Quickstart)](https://docs.dlocal.com/docs/make-a-test-payment)
- [Enable Live Mode](https://docs.dlocal.com/docs/enable-live-mode)
- [Initial Settings](https://docs.dlocal.com/docs/initial-settings)
- [Status Page](https://dlocal.statuspage.io/)
- [Blog](https://dlocal.com/blog/)
- [Press Releases](https://dlocal.com/press-releases/)
- [Investor Relations (NASDAQ: DLO)](https://investor.dlocal.com/)
- [Careers](https://dlocal.com/careers/)
- [Sign Up / Contact Sales](https://dlocal.com/contact-sales/)
- [Support](http://intercom.help/end-user-team-faqs/en)
- [Terms of Service](https://dlocal.com/terms-and-conditions/)
- [Privacy Policy](https://dlocal.com/privacy-policy/)

### Authentication and Compliance
- [Generate A Signature](https://docs.dlocal.com/docs/generate-signature)
- [Get API Credentials](https://docs.dlocal.com/docs/get-api-credentials-new)
- [PCI Compliance](https://docs.dlocal.com/docs/pci-compliance)

### LLM and Agent Integration
- [Using LLMs with dLocal (built-in MCP Server)](https://docs.dlocal.com/docs/using-llms)
- [LLM-friendly docs index](https://docs.dlocal.com/llms.txt)
- [Postman Collection](https://docs.dlocal.com/reference/postman-api-collection)

### SDKs and Client Libraries
- [dLocal GitHub Organization](https://github.com/dlocal)
- [dLocal Direct iOS SDK](https://github.com/dlocal/dlocal-direct-ios-sdk)
- [dLocal Direct Android SDK](https://github.com/dlocal/dlocal-direct-android-sdk)
- [dLocal Mobile Checkout iOS SDK](https://github.com/dlocal/mobile-checkout-sdk-ios)
- [dLocal Mobile Checkout Android SDK](https://github.com/dlocal/mobile-checkout-sdk-android)
- [dLocal Web Drop-In Android SDK](https://github.com/dlocal/web-drop-in-sdk-android)
- [dLocal Data Collector iOS SDK](https://github.com/dlocal/data-collector-sdk-ios)
- [dLocal Data Collector Android SDK](https://github.com/dlocal/data-collector-sdk-android)
- [dLocal Data Collector Capacitor Plugin](https://github.com/dlocal/dlocal-data-collector-capacitor-plugin)
- [dLocal Direct JS-Native Integration](https://github.com/dlocal/dlocal-direct-js-native-integration)
- [dLocal SmartFields Examples](https://github.com/dlocal/smart-fields-examples)
- [dLocal Starter Code Examples](https://github.com/dlocal/Starter-Code-Examples)
- [dlocal.js (SmartFields)](https://docs.dlocal.com/reference/including-dlocaljs)

### Errors and Troubleshooting
- [Payment Status Codes](https://docs.dlocal.com/reference/payment-status-codes)
- [HTTP Errors — Payments](https://docs.dlocal.com/reference/http-errors-payments)
- [HTTP Errors — Refunds](https://docs.dlocal.com/reference/http-errors-refunds)
- [HTTP Errors — Cards](https://docs.dlocal.com/reference/http-errors-cards)
- [Error Codes — Payouts V3](https://docs.dlocal.com/reference/error-codes-payouts-v3)
- [Troubleshooting Integration](https://docs.dlocal.com/reference/troubleshooting-integration)
- [Troubleshooting Signature](https://docs.dlocal.com/reference/troubleshooting-signature)

### Cross-Cutting Generated Artifacts
- [Spectral Rules](rules/d-local-rules.yml)
- [Vocabulary](vocabulary/d-local-vocabulary.yml)
- [JSON-LD Context](json-ld/d-local-context.jsonld)
- [Naftiko Capability — Emerging-Markets Payments Workflow](capabilities/emerging-markets-payments.yaml)
- [API Commons Plans](plans/d-local-plans-pricing.yml)
- [API Commons Rate Limits](rate-limits/d-local-rate-limits.yml)
- [FinOps (FOCUS-aligned)](finops/d-local-finops.yml)

## Features

- 1,000+ local payment methods across 60+ countries in Latin America, Africa, the Middle East, and Asia
- Single REST API for Payins, Payouts, Refunds, Cards, Chargebacks, Enrollments, and Exchange Rates
- Payments API authenticated with V2-HMAC-SHA256 signature (X-Login, X-Trans-Key, X-Date)
- Payouts V3 API with OAuth2 Bearer tokens, FX quoting, on-hold release, and explicit fee breakdown
- dLocal for Platforms (marketplace) API for sub-merchant onboarding, KYC, bank accounts, balances, and transfers
- KYC Verifications API for remitter, beneficiary, and standalone identity checks
- Brazilian Pix Automático recurring, Pix Biometrics, and SmartPix
- India RBI-compliant card network tokenization
- African M-Pesa and Mobile Money integration
- 3D Secure 2.x and card network token support
- SmartFields client-side tokenization via dlocal.js
- Defense Suite fraud-management add-on
- Hosted Checkout (dLocal Go), Payment Links, Virtual Accounts
- Sandbox environment with chargeback simulation
- Webhook notifications for every async event
- Built-in dLocal MCP Server for LLM-assisted integration

## Use Cases

- Global SaaS subscription billing in emerging markets
- Cross-border payroll and contractor payouts
- Marketplace and platform payouts
- Consumer remittances
- Travel and ride-hailing collections and disbursements
- E-commerce expansion via Boleto, OXXO, SPEI, Pix
- Stablecoin-rail cross-border settlement

## Solutions

Payins, Payouts, dLocal for Platforms, Defense Suite, Invoice Collection, Stablecoin Full, dLocal Direct, SmartFields, dLocal Go, Payment Links.

## Maintainer

- **Kin Lane** — info@apievangelist.com — [apievangelist.com](https://apievangelist.com)
