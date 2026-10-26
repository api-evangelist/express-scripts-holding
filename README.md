# Express Scripts Holding (express-scripts-holding)

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

Express Scripts is a pharmacy benefit management (PBM) company, now part of Cigna's Evernorth Health Services, that processes prescription claims and provides home delivery and specialty pharmacy services for clients including health plans and employers. The Express Scripts Developer Portal exists for partner and client integrations, but its API catalog is not openly published; access is gated to authenticated partners.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/express-scripts-holding/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Producing
- **Access:** 3rd-Party (partner-approved)

## Tags:

 - Health, Healthcare, Pharmacy, Pharmacy Benefit Management, Prescriptions, Claims, Fortune 100

## Timestamps

- **Created:** 2026-03-24
- **Modified:** 2026-09-07

## APIs

**Express Scripts Partner APIs** — `https://api.express-scripts.io`
([reference](https://developer.express-scripts.com/service-apis))

Express Scripts operates a real partner API estate: a production gateway at
`api.express-scripts.io`, a separate sandbox gateway at `api-sandbox.express-scripts.io`,
and its own OAuth 2.0 / OpenID Connect authorization server on an Express Scripts Okta
tenant. Both gateway hosts answer HTTP 401 to every anonymous request, including
`/.well-known/*` paths, so the gateway authenticates before it routes.

**No API contract is published publicly.** No OpenAPI, GraphQL SDL, AsyncAPI, Protobuf or
WSDL is reachable at any anonymous URL. The developer portal renders client-side, its
content backend returns `{"message":"Missing Authentication Token"}` (HTTP 403) on every
path, and the portal's own deployed configuration sets `"public-specs": false` — so
specifications are visible only to approved partners after sign-in.

What Express Scripts *does* publish anonymously are its OAuth discovery documents, captured
verbatim in `well-known/`: OpenID Connect discovery and RFC 8414 authorization-server
metadata advertising PKCE (S256), DPoP, PAR, the device grant, CIBA, token introspection,
revocation and dynamic client registration.

> **Not Express Scripts.** The developer portal shares one codebase with the Cigna and
> Evernorth portals, and its bundle names two FHIR base URLs on `digitaledge.cigna.com`.
> Both CapabilityStatements were fetched and both declare `publisher: "Cigna, Inc."`. Those
> are Cigna's CMS Interoperability APIs and are deliberately **not** attributed to Express
> Scripts.

## Common Properties

- [Website](https://www.express-scripts.com)
- [Developer Portal](https://developer.express-scripts.com/)
- [Parent Company](https://www.evernorth.com/)
- [GitHub Organization](https://github.com/ExpressScripts)
- [Terms of Service](https://www.express-scripts.com/terms-of-use)
- [Privacy Policy](https://www.evernorth.com/privacy-policy)
- [Support](https://www.express-scripts.com/contact-us)
- [Help Center](https://www.express-scripts.com/frequently-asked-questions)
- [Trust Center](https://trust.express-scripts.com/) — SOC 2, PCI DSS, HIPAA
- [Vulnerability Disclosure](https://www.cigna.com/legal/members/responsible-vulnerability-disclosure)

Machine-readable artifacts in this repository: `well-known/`, `authentication/`, `scopes/`,
`conformance/`, `sandbox/`, `lifecycle/`, `plans/`, `rate-limits/`, `packages/`, `llms/`,
`security/`.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
