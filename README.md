# Akash Network

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

Akash Network is a decentralized cloud computing marketplace that connects users with underutilized compute capacity from data centers and bare-metal providers worldwide. Deployments run as containerized workloads (Docker/Kubernetes) on provider hardware at 60-85% lower cost than traditional cloud providers via competitive bidding.

## APIs Cataloged

| API | Base URL | Auth | Description |
|-----|----------|------|-------------|
| Console Deployment API | `https://console-api.akash.network` | x-api-key | Programmatic deployment management with managed wallets and credit-card billing |
| Console Network Data API | `https://console-api.akash.network` | None (public) | Provider discovery, GPU availability, network stats |
| Blockchain REST API | `https://api.akashnet.net` | None / wallet | Direct Cosmos SDK + Akash module queries via gRPC-Gateway |
| AkashML Inference API | `https://api.akashml.com` | Bearer token | OpenAI-compatible LLM inference on decentralized compute |

## Key Concepts

- **SDL (Stack Definition Language)**: YAML manifest format for describing containerized deployments on Akash
- **Deployment**: A deployed workload with an associated escrow account on-chain
- **Bid**: Provider offer to run a deployment at a given price
- **Lease**: Accepted bid; provider runs the deployment for the duration of the lease
- **Escrow**: On-chain account holding AKT/USDC to pay for an active deployment

## Quick Links

- Documentation: https://akash.network/docs
- API Documentation: https://akash.network/docs/api-documentation/getting-started/
- Console: https://console.akash.network
- AkashML: https://akashml.com
- GitHub: https://github.com/akash-network
- Discord: https://discord.akash.network
- Stats: https://stats.akash.network

## Repository Structure

```
akash/
  apis.yml              # APIs.json 0.19 catalog entry
  plans/
    plans.yml           # Pricing plan details
  rate-limits/
    rate-limits.yml     # Rate limit specifications per API
  finops/
    finops.yml          # FinOps guidance, cost drivers, and pricing tables
  README.md             # This file
```
