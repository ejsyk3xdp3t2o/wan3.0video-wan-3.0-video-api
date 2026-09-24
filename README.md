# Wan 3.0 Video API (wan-3.0-video / wan3.0video) — api guide with published pricing

> **480P $0.0329; 720P $0.0658; default $0.1315** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **wan-3.0-video** — also written **wan3.0video** or **wan 3.0 video**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `480P` | $0.0329 |
| `720P` | $0.0658 |
| `default` | $0.1315 |
| `1080P` | $0.1315 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $3.288 |
| 1,000 | $32.88 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/videos/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"wan3.0-video","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
