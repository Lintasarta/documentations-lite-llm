# Metrics

## Metrics & Observability

Custom performance metrics added:
- TTFT (Time To First Token)
- TPS (Tokens Per Second)
- Latency

![Lite LLM Metrics Dashboard](2.png)

---

## Metrics Storage

Metrics are stored in Redis instead of in-memory.

This is needed to aggregate metrics across multiple replicas.

Native LiteLLM metrics break when running more than one replica because:
- Each pod keeps metrics in its own memory
- No global aggregation exists by default

![Metrics Storage Before and After](3.png)

---

## Metrics Collection

Metrics are scraped from the service using Cortex.
