# dLocal (d-local)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

dLocal (NASDAQ: DLO) is a Uruguay-headquartered emerging-markets payment
infrastructure platform connecting global merchants with billions of
consumers across 60+ countries in Latin America, Africa, the Middle East,
and Asia. dLocal exposes a unified set of REST APIs for accepting payments
(Payins) via 1,000+ local methods, disbursing funds (Payouts V3) to
beneficiaries via local rails, tokenizing cards, managing marketplace
sub-merchants (dLocal for Platforms), performing KYC verifications,
handling chargebacks, enrolling users for recurring Pix flows, and pulling
real-time exchange rates. Native iOS and Android SDKs are published as
open source on GitHub.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/d-local/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/d-local/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming

## Tags

- Payments
- Payouts
- EmergingMarkets
- LatAm
- Africa
- Asia
- FX
- Fintech

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### dLocal Payments API

Create, retrieve, cancel, and authorize payments using 1,000+ local
payment methods including cards, Pix, UPI, M-Pesa, Boleto, OXXO, SPEI,
mobile money, cash vouchers, BNPL, wallets, and QR codes across 60+
countries. Authenticated with V2-HMAC-SHA256 signature.

- **Human URL:** [https://docs.dlocal.com/reference/create-payment](https://docs.dlocal.com/reference/create-payment)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- Payments
- Payins
- Cards

#### Properties

- [Documentation](https://docs.dlocal.com/reference/create-payment)
- [Documentation](https://docs.dlocal.com/reference/retrieve-a-payment)
- [Getting Started](https://docs.dlocal.com/docs/make-payment)
- [OpenAPI](openapi/d-local-payments-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-payments-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-payments-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/payments-payment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/payments-payment-structure.json)
- [Example](examples/payments-create-payment-example.json)
- [Example](examples/payments-retrieve-payment-example.json)
- [Example](examples/payments-pix-example.json)

### dLocal Refunds API

Create, retrieve, and inspect refunds against previously successful
payments. Refunds may be full or partial and are settled in the
original payment currency.

- **Human URL:** [https://docs.dlocal.com/reference/make-a-refund](https://docs.dlocal.com/reference/make-a-refund)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- Refunds
- Payments

#### Properties

- [Documentation](https://docs.dlocal.com/reference/make-a-refund)
- [Documentation](https://docs.dlocal.com/docs/refunds)
- [OpenAPI](openapi/d-local-refunds-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-refunds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-refunds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/refunds-refund-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/refunds-make-refund-example.json)

### dLocal Cards API

Securely tokenize cards (server-side) for repeat usage. Returns a
card_id token consumable by subsequent Payments and Authorizations.

- **Human URL:** [https://docs.dlocal.com/reference/create-a-card](https://docs.dlocal.com/reference/create-a-card)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- Cards
- Tokenization

#### Properties

- [Documentation](https://docs.dlocal.com/reference/create-a-card)
- [Documentation](https://docs.dlocal.com/docs/saving-cards)
- [OpenAPI](openapi/d-local-cards-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-cards-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-cards-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/cards-card-token-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/cards-create-card-example.json)

### dLocal Payouts V3 API

Disburse funds to beneficiaries across 60+ countries via local bank
transfers, instant payments, cards, mobile money, and cash pick-up.
Includes balance, quoting, release, and cancel operations. Uses
OAuth2 Bearer authentication.

- **Human URL:** [https://docs.dlocal.com/reference/requesting-payout-v3](https://docs.dlocal.com/reference/requesting-payout-v3)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- Payouts
- Disbursements
- Crossborder

#### Properties

- [Documentation](https://docs.dlocal.com/reference/requesting-payout-v3)
- [Documentation](https://docs.dlocal.com/docs/overview-payouts-v3)
- [Authentication](https://docs.dlocal.com/reference/security-payouts-v3)
- [OpenAPI](openapi/d-local-payouts-v3-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-payouts-v3-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-payouts-v3-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/payouts-v3-payout-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/payouts-v3-payout-structure.json)
- [Example](examples/payouts-v3-request-payout-example.json)
- [Example](examples/payouts-v3-get-balance-example.json)

### dLocal For Platforms API

The dLocal for Platforms (marketplace) API onboards sub-merchant
accounts, manages KYC, attaches bank accounts, settles inter-account
transfers, and reports balances. Designed for marketplaces and
platforms that hold funds on behalf of sub-users.

- **Human URL:** [https://docs.dlocal.com/docs/platforms-overview](https://docs.dlocal.com/docs/platforms-overview)
- **Base URL:** `https://marketplace-api.dlocal.com`

#### Tags

- Marketplace
- Platforms
- Accounts
- KYC

#### Properties

- [Documentation](https://docs.dlocal.com/docs/platforms-overview)
- [Documentation](https://docs.dlocal.com/reference/create-account-v2-platforms-1)
- [Documentation](https://docs.dlocal.com/reference/notifications-v2-platforms)
- [OpenAPI](openapi/d-local-platforms-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-platforms-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-platforms-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/platforms-account-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/platforms-create-account-example.json)

### dLocal KYC Verifications API

Create and manage KYC verifications across remittance, payouts-on-hold,
payins-on-hold, and standalone flows. Receives asynchronous status
updates via webhook.

- **Human URL:** [https://docs.dlocal.com/docs/kyc-verifications-overview](https://docs.dlocal.com/docs/kyc-verifications-overview)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- KYC
- Compliance
- Verifications

#### Properties

- [Documentation](https://docs.dlocal.com/docs/kyc-verifications-overview)
- [Documentation](https://docs.dlocal.com/docs/kyc-verifications-process)
- [Documentation](https://docs.dlocal.com/reference/create-verification-1)
- [OpenAPI](openapi/d-local-kyc-verifications-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-kyc-verifications-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-kyc-verifications-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/kyc-create-verification-example.json)

### dLocal Chargebacks API

Retrieve chargeback details and status, simulate chargebacks in the
sandbox, and receive asynchronous chargeback notifications via webhook.

- **Human URL:** [https://docs.dlocal.com/reference/retrieve-a-chargeback](https://docs.dlocal.com/reference/retrieve-a-chargeback)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- Chargebacks
- Disputes
- Payments

#### Properties

- [Documentation](https://docs.dlocal.com/reference/retrieve-a-chargeback)
- [Documentation](https://docs.dlocal.com/docs/chargebacks)
- [Documentation](https://docs.dlocal.com/docs/chargeback-categories)
- [OpenAPI](openapi/d-local-chargebacks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-chargebacks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-chargebacks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### dLocal Enrollments API

Enroll payers for recurring Pix Automático, Pix Biometrics, and
SmartPix transactions. Once enrolled, payers can be charged
repeatedly without re-authorization.

- **Human URL:** [https://docs.dlocal.com/reference/create-enrollment](https://docs.dlocal.com/reference/create-enrollment)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- Enrollments
- Recurring
- Pix
- Brazil

#### Properties

- [Documentation](https://docs.dlocal.com/reference/create-enrollment)
- [Documentation](https://docs.dlocal.com/docs/brazil-pix-automatico)
- [Documentation](https://docs.dlocal.com/docs/brazil-pix-biometrics)
- [Documentation](https://docs.dlocal.com/docs/brazil-smartpix)
- [OpenAPI](openapi/d-local-enrollments-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-enrollments-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-enrollments-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### dLocal Exchange Rates API

Retrieve real-time FX rates between settlement currencies and local
currencies before creating a payment or payout.

- **Human URL:** [https://docs.dlocal.com/reference/get-an-exchange-rate](https://docs.dlocal.com/reference/get-an-exchange-rate)
- **Base URL:** `https://api.dlocal.com`

#### Tags

- FX
- ExchangeRates

#### Properties

- [Documentation](https://docs.dlocal.com/reference/get-an-exchange-rate)
- [OpenAPI](openapi/d-local-exchange-rates-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/d-local-exchange-rates-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/d-local-exchange-rates-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/exchange-rates-get-rate-example.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://dlocal.com/)
- [Documentation](https://docs.dlocal.com/)
- [API Reference](https://docs.dlocal.com/reference/api)
- [Getting Started](https://docs.dlocal.com/docs/get-started)
- [Quickstart](https://docs.dlocal.com/docs/make-a-test-payment)
- [Documentation](https://docs.dlocal.com/docs/enable-live-mode)
- [Documentation](https://docs.dlocal.com/docs/initial-settings)
- [Authentication](https://docs.dlocal.com/docs/generate-signature)
- [Authentication](https://docs.dlocal.com/docs/get-api-credentials-new)
- [Compliance](https://docs.dlocal.com/docs/pci-compliance)
- [Documentation](https://docs.dlocal.com/docs/using-llms)
- [Documentation](https://docs.dlocal.com/llms.txt)
- [SDK](https://docs.dlocal.com/reference/postman-api-collection)
- [Status Page](https://dlocal.statuspage.io/)
- [Blog](https://dlocal.com/blog/)
- [Sign Up](https://dlocal.com/contact-sales/)
- [Resources](https://dlocal.com/careers/)
- [Newsletter](https://dlocal.com/press-releases/)
- [Resources](https://investor.dlocal.com/)
- [Terms of Service](https://dlocal.com/terms-and-conditions/)
- [Privacy Policy](https://dlocal.com/privacy-policy/)
- [Support](http://intercom.help/end-user-team-faqs/en)
- [GitHub Organization](https://github.com/dlocal)
- [SDK](https://github.com/dlocal/dlocal-direct-ios-sdk)
- [SDK](https://github.com/dlocal/dlocal-direct-android-sdk)
- [SDK](https://github.com/dlocal/mobile-checkout-sdk-ios)
- [SDK](https://github.com/dlocal/mobile-checkout-sdk-android)
- [SDK](https://github.com/dlocal/web-drop-in-sdk-android)
- [SDK](https://github.com/dlocal/data-collector-sdk-ios)
- [SDK](https://github.com/dlocal/data-collector-sdk-android)
- [SDK](https://github.com/dlocal/dlocal-data-collector-capacitor-plugin)
- [SDK](https://github.com/dlocal/dlocal-direct-js-native-integration)
- [Code Examples](https://github.com/dlocal/smart-fields-examples)
- [Code Examples](https://github.com/dlocal/Starter-Code-Examples)
- [SDK](https://docs.dlocal.com/reference/including-dlocaljs)
- [Troubleshooting](https://docs.dlocal.com/reference/troubleshooting-integration)
- [Troubleshooting](https://docs.dlocal.com/reference/troubleshooting-signature)
- [Documentation](https://docs.dlocal.com/reference/payment-status-codes)
- [Errors](https://docs.dlocal.com/reference/http-errors-payments)
- [Errors](https://docs.dlocal.com/reference/http-errors-refunds)
- [Errors](https://docs.dlocal.com/reference/http-errors-cards)
- [Errors](https://docs.dlocal.com/reference/error-codes-payouts-v3)
- [Documentation](https://docs.dlocal.com/reference/country-reference)
- [Documentation](https://docs.dlocal.com/docs/overview-payins)
- [Documentation](https://docs.dlocal.com/docs/overview-payouts-v3)
- [Documentation](https://docs.dlocal.com/docs/platforms-overview)
- [Documentation](https://docs.dlocal.com/docs/overview-smart-fields)
- [Documentation](https://docs.dlocal.com/docs/integrate-checkout)
- [Documentation](https://docs.dlocal.com/docs/payment-links)
- [Documentation](https://docs.dlocal.com/docs/fraud-prevention)
- [Spectral Rules](rules/d-local-rules.yml)
- [Vocabulary](vocabulary/d-local-vocabulary.yml)
- [JSON-LD](json-ld/d-local-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Plans](plans/d-local-plans-pricing.yml)
- [Rate Limits](rate-limits/d-local-rate-limits.yml)
- [Fin Ops](finops/d-local-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
