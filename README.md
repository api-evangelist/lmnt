# LMNT (lmnt)

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

LMNT is a text-to-speech API platform delivering ultra-low latency voice synthesis with streaming audio output designed for real-time conversational AI applications. The platform provides a Speech API for standard text-to-speech generation and a Speech Sessions API for WebSocket-based real-time streaming integrated with LLM pipelines, achieving latency under 300 milliseconds. LMNT supports 31 languages and offers voice cloning from as little as five seconds of audio, with its Blizzard 2 model optimized for accuracy, expressiveness, and pronunciation across diverse accents and styles.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lmnt/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lmnt/refs/heads/main/apis.yml)

**Naftiko:** [https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=lmnt-api-evangelist&utm_content=repo](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=lmnt-api-evangelist&utm_content=repo)

## Tags

- text-to-speech
- voice synthesis
- voice cloning
- audio streaming
- conversational AI
- low latency
- real-time audio

## APIs

### LMNT Speech API

REST API for converting text to speech audio, supporting streaming binary audio output, 31 languages, voice cloning, word timestamps, and configurable expressiveness parameters. Endpoint: `POST /v1/ai/speech/bytes`. Authentication via `X-API-Key` header. Maximum 5,000 characters per request.

- **Documentation:** [https://docs.lmnt.com/api-reference/speech/synthesize-speech-bytes](https://docs.lmnt.com/api-reference/speech/synthesize-speech-bytes)

### LMNT Speech Sessions API

WebSocket-based real-time speech generation API for streaming LLM text output to synthesized audio with reset-latency support for conversational AI applications requiring interrupt handling. Uses API version 1.2 with word timestamp improvements.

- **Documentation:** [https://docs.lmnt.com/api-reference/speech/generate-speech-session](https://docs.lmnt.com/api-reference/speech/generate-speech-session)

## Plans, Rate Limits, and FinOps

### Plans

LMNT offers four self-serve pricing tiers plus a custom enterprise option:

| Plan | Price | Included Characters | Overage Rate |
|---|---|---|---|
| Free | $0/month | 15,000 | None (quota hard stop) |
| Indie | $10/month | 200,000 | $0.05 per 1K characters |
| Pro | $49/month | 1,250,000 | $0.045 per 1K characters |
| Premium | $199/month | 5,700,000 | $0.035 per 1K characters |
| Enterprise | Custom | Custom | Negotiated |

Paid plans (Indie and above) include a commercial license and unlimited voice clones.

- **Plans file:** [plans/lmnt-plans-pricing.yml](plans/lmnt-plans-pricing.yml)

### Rate Limits

Paid plans carry no concurrency or request rate limits. Free accounts are subject to monthly character quotas. Individual requests are capped at 5,000 characters of input. API v1.1+ returns a `request-id` header on every response.

- **Rate Limits file:** [rate-limits/lmnt-rate-limits.yml](rate-limits/lmnt-rate-limits.yml)

### FinOps

LMNT uses a subscription plus metered overage model billed monthly in USD. The primary cost meter is characters synthesized. Upgrading subscription tiers reduces per-character overage rates and provides larger included allotments.

- **FinOps file:** [finops/lmnt-finops.yml](finops/lmnt-finops.yml)

## Timestamps

- **Created:** 2026-06-12
- **Modified:** 2026-06-12

## Common Properties

| Type | URL |
|---|---|
| Website | [https://www.lmnt.com/](https://www.lmnt.com/) |
| Documentation | [https://docs.lmnt.com/](https://docs.lmnt.com/) |
| GitHub Organization | [https://github.com/lmnt-com](https://github.com/lmnt-com) |
| LinkedIn | [https://www.linkedin.com/company/lmnt](https://www.linkedin.com/company/lmnt) |
| X | [https://x.com/lmnt_com](https://x.com/lmnt_com) |
| Pricing | [https://www.lmnt.com/pricing](https://www.lmnt.com/pricing) |
| Changelog | [https://docs.lmnt.com/changelog/overview](https://docs.lmnt.com/changelog/overview) |
| Plans | [plans/lmnt-plans-pricing.yml](plans/lmnt-plans-pricing.yml) |
| Rate Limits | [rate-limits/lmnt-rate-limits.yml](rate-limits/lmnt-rate-limits.yml) |
| FinOps | [finops/lmnt-finops.yml](finops/lmnt-finops.yml) |

## Maintainers

- **Kin Lane** — [kin@apievangelist.com](mailto:kin@apievangelist.com)
