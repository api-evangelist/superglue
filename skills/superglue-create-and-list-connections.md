---
name: superglue-create-and-list-connections
description: Create a new connection and then list all accessible connections.
api: openapi/superglue-openapi.yml
operations:
- createConnection
- listConnections
generated: '2026-10-19'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/superglue-openapi.yml ; every operationId checked against the contract
---

# superglue-create-and-list-connections

Create a new connection and then list all accessible connections.

## Steps

1. 1. Call `createConnection` with the required request body fields for the new connection.
2. 2. Call `listConnections` with optional query parameters (e.g., `page`, `pageSize`) to retrieve the updated list of connections.

## Rules

- Auth: Include the `ApiKeyAuth` header (`Authorization: Bearer <api_key>`).
- Pagination: `listConnections` supports `page` and `pageSize` query parameters for paginated results.
