# Healthcare.com

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
