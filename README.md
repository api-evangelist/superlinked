# Superlinked (superlinked)

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
