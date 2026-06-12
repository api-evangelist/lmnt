# LMNT (lmnt)

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
