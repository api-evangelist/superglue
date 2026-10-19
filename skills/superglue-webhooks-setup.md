---
name: superglue-webhooks-setup
description: Verify a webhook endpoint and then trigger it to handle incoming events.
api: openapi/superglue-openapi.yml
operations:
- verifyWebhook
- triggerWebhook
generated: '2026-10-19'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/superglue-openapi.yml ; every operationId checked against the contract
---

# superglue-webhooks-setup

Verify a webhook endpoint and then trigger it to handle incoming events.

## Steps

1. 1. Call `verifyWebhook` with the path parameter `toolId` to complete the webhook challenge verification.
2. 2. Call `triggerWebhook` with the path parameter `toolId` (and request body as defined by the webhook payload) to handle an incoming webhook.

## Rules

- Use the `ApiKeyAuth` HTTP header for authentication on both calls.
- Both operations require the `toolId` path parameter.
