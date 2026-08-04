# Superlinked (superlinked)

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

Superlinked is an open-source Python framework for building vector-compute pipelines that encode structured and unstructured data into multi-modal embeddings for retrieval, recommendations, RAG, and analytics. When deployed via the Superlinked Server, the framework auto-generates a REST API - ingestion and query endpoints derived directly from your schema, index, and query definitions - and connects to external vector databases. A managed Superlinked Cloud is available in early access.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/superlinked/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/superlinked/refs/heads/main/apis.yml)

## Tags

- Vectors
- Embeddings
- Vector Search
- Retrieval
- Recommendations
- RAG

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Superlinked Ingestion API

Schema-generated REST ingestion endpoint exposed by the Superlinked Server. Each schema defined in your app produces a POST /api/v1/ingest/{schema} endpoint that accepts records, computes multi-modal embeddings, and writes vectors to the configured vector database. Endpoints and request bodies are generated from your Python schema definitions, not hand-authored.

- **Human URL:** [https://github.com/superlinked/superlinked](https://github.com/superlinked/superlinked)
- **Base URL:** `http://localhost:8080/api/v1`

#### Tags

- Ingestion
- Vectors
- Schema

#### Properties

- [Documentation](https://github.com/superlinked/superlinked)
- [API Reference](https://github.com/superlinked/superlinked)
- [OpenAPI](openapi/superlinked-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/superlinked/superlinked)
- [Postman Collection](collections/superlinked.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/superlinked.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Superlinked Query API

Schema-generated REST query endpoint exposed by the Superlinked Server. Each RestQuery you register produces a POST /api/v1/search/{query_name} endpoint whose request body parameters (natural_query, weights, filters, limit) are derived from the query definition. Returns ranked results from the connected vector store.

- **Human URL:** [https://github.com/superlinked/superlinked](https://github.com/superlinked/superlinked)
- **Base URL:** `http://localhost:8080/api/v1`

#### Tags

- Query
- Search
- Retrieval

#### Properties

- [Documentation](https://github.com/superlinked/superlinked)
- [API Reference](https://github.com/superlinked/superlinked)
- [OpenAPI](openapi/superlinked-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/superlinked/superlinked)
- [Postman Collection](collections/superlinked.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/superlinked.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Superlinked Data Loader API

Server endpoints for triggering and monitoring configured batch data loaders - POST /data-loader/{name}/run starts a load and GET /data-loader/{name}/status reports progress - used to backfill vectors from files or external sources.

- **Human URL:** [https://github.com/superlinked/superlinked](https://github.com/superlinked/superlinked)
- **Base URL:** `http://localhost:8080`

#### Tags

- Data Loader
- Batch
- Ingestion

#### Properties

- [Documentation](https://github.com/superlinked/superlinked)
- [OpenAPI](openapi/superlinked-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/superlinked/superlinked)
- [Postman Collection](collections/superlinked.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/superlinked.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Superlinked Framework (Python)

The open-source Apache-2.0 Python framework (pip install superlinked) used to declare Schema, Space, Index, Query, Source, and Executor objects. The same definitions run in-memory for prototyping or power the Superlinked Server, which generates the REST API. This is a library/SDK surface, not an HTTP API.

- **Human URL:** [https://github.com/superlinked/superlinked](https://github.com/superlinked/superlinked)
- **Base URL:** `https://pypi.org/project/superlinked`

#### Tags

- Framework
- Python
- Embeddings

#### Properties

- [Documentation](https://github.com/superlinked/superlinked)
- [GitHub](https://github.com/superlinked/superlinked)
- [Postman Collection](collections/superlinked.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/superlinked.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Superlinked Cloud

Managed, production-scale hosting of Superlinked-powered apps, available in early access via a sales-led demo. Runs the same schema-generated REST surface as the self-hosted Superlinked Server without the user operating the infrastructure.

- **Human URL:** [https://www.superlinked.com](https://www.superlinked.com)
- **Base URL:** `https://www.superlinked.com`

#### Tags

- Cloud
- Managed
- Vectors

#### Properties

- [Documentation](https://www.superlinked.com)
- [Postman Collection](collections/superlinked.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/superlinked.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/superlinked)
- [LinkedIn](https://www.linkedin.com/company/superlinked)
- [Website](https://www.superlinked.com)
- [Documentation](https://github.com/superlinked/superlinked)
- [Plans](plans/superlinked-plans-pricing.yml)
- [Rate Limits](rate-limits/superlinked-rate-limits.yml)
- [Fin Ops](finops/superlinked-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
