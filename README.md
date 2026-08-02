# Healthcare.com

Healthcare.com (HealthCare, Inc.) is a privately held, non-government health insurance
marketplace and distribution platform founded in 2014. Consumers use healthcare.com to find,
compare and enroll in ACA/under-65 individual health plans, Medicare Advantage and Medicare
Supplement plans, and specialty coverage. Distributors, FMOs, MGAs and agents use its
**Autopilot** machine-learning enrollment acquisition platform, which matches high-intent
shoppers to distributor partners with predictive scoring and value-based lead pricing. Its
**Pivot Health** subsidiary develops and markets proprietary short-term medical, fixed
indemnity and supplemental gap products with A-rated carriers. Insurance is sold through
Healthcare.com Insurance Services, LLC. Not affiliated with HealthCare.gov.

- https://www.healthcare.com/
- https://www.healthcare.com/about-company
- https://www.pivothealth.com/

## API surface

**No public developer API.** As of the 2026-08-01 enrichment pass, Healthcare.com publishes
no developer portal, API reference, OpenAPI/AsyncAPI/GraphQL contract, SDK, CLI, Postman
collection, MCP server or A2A agent card. `api.healthcare.com` is a live first-party API host
(HTTP/2, HSTS with `preload`) but it is private: the root returns HTTP 418 with an empty body
and unknown paths return a plain-text 404. `autopilot.healthcare.com` is an authenticated
Retool application. `developer.`, `developers.` and `docs.healthcare.com` do not resolve.

The full probe record — every `/.well-known/*` path, OpenAPI/GraphQL/MCP/agent-card candidate,
and developer-host lookup — is in `well-known/healthcare-com-well-known.yml`. Note that
`www.healthcare.com` is a Next.js SPA whose catch-all answers **HTTP 200 with an HTML shell
for every unknown path**, so 200s on `/.well-known/*`, `/openapi.json` and
`/vulnerability-disclosure/` are soft 404s, not hits.

## Artifacts

| Path | Type | Method |
|---|---|---|
| `apis.yml` | APIs.json 0.20 index | — |
| `well-known/healthcare-com-well-known.yml` | well-known + contract-discovery probe record (all misses) | probed |
| `security/healthcare-com-domain-security.yml` | TLS/HSTS/DNSSEC/CAA/SPF/DMARC posture | probed |
| `lifecycle/healthcare-com-lifecycle.yml` | versioning / deprecation / status page | probed |
| `llms/healthcare-com-llms.txt` | llms.txt for agents | generated |

Not applicable (nothing published to harvest, and nothing fabricated): `openapi/`, `asyncapi/`,
`graphql/`, `mcp/`, `a2a/`, `skills/`, `packages/`, `cli/`, `components/`, `sandbox/`,
`overlays/`, `grpc/`, `scopes/`, `authentication/`, `conventions/`, `errors/`, `data-model/`,
`changelog/`, `conformance/`.
