---
name: superglue-get-run-results
description: Retrieve a completed run's status, results, and download its artifact files.
api: openapi/superglue-openapi.yml
operations:
- getRun
- getRunResults
- listRunFiles
- getRunFileDownload
generated: '2026-10-19'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/superglue-openapi.yml ; every operationId checked against the contract
---

# superglue-get-run-results

Retrieve a completed run's status, results, and download its artifact files.

## Steps

1. 1. Call `getRun` with path parameter `runId` to obtain the run's status and metadata.
2. 2. Call `getRunResults` with the same `runId` to fetch the full run results.
3. 3. Call `listRunFiles` with `runId` to list all file artifacts produced by the run.
4. 4. For each file returned, call `getRunFileDownload` with `runId` and the file's `fileKey` to obtain a download URL.

## Rules

- Auth: Include an `Authorization` header using the `ApiKeyAuth` scheme (HTTP API key).
- Idempotency: The `cancelRun` operation is not used in this skill; all other calls are safe and idempotent.
- Pagination: If `listRunFiles` returns paginated results, follow the `next` cursor provided in the response to retrieve all files.
