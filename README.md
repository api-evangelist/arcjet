# Arcjet (arcjet)

Arcjet is a security-as-code platform for developers, delivering rate limiting, bot detection, email validation, sensitive-information detection, and a Shield WAF as building blocks embedded directly in application code via SDKs. The SDK is the primary interface; it runs a local WebAssembly analysis module and calls Arcjet's Decide service - a Connect/gRPC (protobuf) decision API at decide.arcjet.com - for stateful decisions like rate limiting and advanced bot detection.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/arcjet/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/arcjet/refs/heads/main/apis.yml)

## Tags

- Security
- Rate Limiting
- Bot Detection
- WAF
- Developer Security

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Arcjet Decide API

The core Connect/gRPC decision service (proto.decide.v1alpha1.DecideService, Decide and Report RPCs) that the Arcjet SDK calls for stateful security decisions. ConnectRPC supports gRPC over HTTP/2 and an HTTP/1.1 + JSON POST fallback to the same service. This is not a typical public REST API - the SDK is the primary, supported interface; the transport is documented here conservatively for reference.

- **Human URL:** [https://docs.arcjet.com/architecture](https://docs.arcjet.com/architecture)
- **Base URL:** `https://decide.arcjet.com`

#### Tags

- Decision
- Protect
- Connect
- gRPC

#### Properties

- [Documentation](https://docs.arcjet.com/architecture)
- [API Reference](https://docs.arcjet.com/reference/nodejs)
- [OpenAPI](openapi/arcjet-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcjet.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcjet.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [GitHub](https://github.com/arcjet/arcjet-js)

### Arcjet Rate Limiting

Token-bucket, fixed-window, and sliding-window rate limiting configured as code and enforced through the SDK, with cross-request state tracked by the cloud Decide service. Limits are keyed on characteristics such as IP, user ID, or API key.

- **Human URL:** [https://docs.arcjet.com/rate-limiting/concepts](https://docs.arcjet.com/rate-limiting/concepts)
- **Base URL:** `https://decide.arcjet.com`

#### Tags

- Rate Limiting
- Throttling
- Quotas

#### Properties

- [Documentation](https://docs.arcjet.com/rate-limiting/concepts)
- [API Reference](https://docs.arcjet.com/rate-limiting/reference)
- [OpenAPI](openapi/arcjet-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Arcjet Bot Detection

Identifies and classifies automated clients, allowing or denying known bots by category. Basic identification runs locally in the SDK WebAssembly module; advanced bot signals are resolved via the cloud Decide service.

- **Human URL:** [https://docs.arcjet.com/bot-protection/concepts](https://docs.arcjet.com/bot-protection/concepts)
- **Base URL:** `https://decide.arcjet.com`

#### Tags

- Bot Detection
- Bots
- Automation

#### Properties

- [Documentation](https://docs.arcjet.com/bot-protection/concepts)
- [API Reference](https://docs.arcjet.com/bot-protection/reference)
- [OpenAPI](openapi/arcjet-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Arcjet Email Validation

Validates email addresses for syntax, deliverability, disposable and no-MX-record domains, and free providers, used to block fake or fraudulent signups. Invoked through the SDK against the Decide service.

- **Human URL:** [https://docs.arcjet.com/email-validation/concepts](https://docs.arcjet.com/email-validation/concepts)
- **Base URL:** `https://decide.arcjet.com`

#### Tags

- Email Validation
- Signup
- Anti-Fraud

#### Properties

- [Documentation](https://docs.arcjet.com/email-validation/concepts)
- [API Reference](https://docs.arcjet.com/email-validation/reference)
- [OpenAPI](openapi/arcjet-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Arcjet Sensitive Information Detection

Detects PII and other sensitive data (emails, phone numbers, credit cards, IP addresses, or custom patterns) in request bodies. Detection runs locally in the SDK WebAssembly module so sensitive content need not leave the application.

- **Human URL:** [https://docs.arcjet.com/sensitive-info/concepts](https://docs.arcjet.com/sensitive-info/concepts)
- **Base URL:** `https://decide.arcjet.com`

#### Tags

- Sensitive Info
- PII
- Data Protection

#### Properties

- [Documentation](https://docs.arcjet.com/sensitive-info/concepts)
- [API Reference](https://docs.arcjet.com/sensitive-info/reference)
- [OpenAPI](openapi/arcjet-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Arcjet Shield WAF

WAF-like protection against common attacks such as SQL injection, cross-site scripting, and other OWASP-style threats, applied to requests flowing through the SDK and evaluated by the Decide service.

- **Human URL:** [https://docs.arcjet.com/shield/concepts](https://docs.arcjet.com/shield/concepts)
- **Base URL:** `https://decide.arcjet.com`

#### Tags

- Shield
- WAF
- Attack Protection

#### Properties

- [Documentation](https://docs.arcjet.com/shield/concepts)
- [API Reference](https://docs.arcjet.com/shield/reference)
- [OpenAPI](openapi/arcjet-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Arcjet SDKs

The primary, supported interface to Arcjet. SDKs ship for Node.js, Next.js, Bun, Deno, SvelteKit, NestJS, Remix, Astro, React Router, Fastify, and Python, each wrapping the Connect/gRPC Decide protocol and the local WebAssembly analysis module.

- **Human URL:** [https://docs.arcjet.com/get-started](https://docs.arcjet.com/get-started)
- **Base URL:** `https://decide.arcjet.com`

#### Tags

- SDK
- JavaScript
- TypeScript
- Python

#### Properties

- [Documentation](https://docs.arcjet.com/get-started)
- [GitHub](https://github.com/arcjet/arcjet-js)
- [SDK](https://www.npmjs.com/package/arcjet)

## Common Properties

- [GitHub Organization](https://github.com/arcjet)
- [LinkedIn](https://www.linkedin.com/company/arcjet)
- [Website](https://arcjet.com)
- [Documentation](https://docs.arcjet.com)
- [Plans](plans/arcjet-plans-pricing.yml)
- [Rate Limits](rate-limits/arcjet-rate-limits.yml)
- [Fin Ops](finops/arcjet-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
