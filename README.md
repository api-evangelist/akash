# Akash Network

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
