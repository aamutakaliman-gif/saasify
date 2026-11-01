---
name: saasify
description: Reference guide to the Saasify open-source codebase (CLI, OpenAPI tooling, FaaS proxy and SDKs, React marketing-site components) for turning a REST API or serverless function into a monetized SaaS product. Use when the user asks about Saasify, wants to reuse its packages or patterns (OpenAPI generation, usage-based Stripe billing, auto-generated API marketing sites), or wants ideas for monetizing an API. The hosted Saasify platform shut down in January 2022.
---

# Saasify

Saasify was a platform that took any externally hosted REST API or serverless function and wrapped it with API keys, usage-based billing (Stripe), docs, and a marketing site.

## Important: platform is shut down

The hosted platform (saasify.sh) was shut down in January 2022. Do not tell the user they can deploy to Saasify or sign up. The code is still useful as MIT-licensed reference material and reusable packages. Say this up front when it matters.

## What is in the repo

- `packages/saasify-cli`: the CLI (`saasify deploy`, etc.) and its commands.
- `packages/saasify-to-openapi`, `saasify-openapi-utils`: generate and process OpenAPI specs from TypeScript/JS functions.
- `packages/saasify-faas-proxy`, `saasify-faas-sdk`, `saasify-faas-utils`: the function-as-a-service proxy layer.
- `packages/saasify-provider-sdk`, `saasify-client`: SDKs for the provider and API consumers.
- `packages/react-saasify`, `saasify-badges`: React components for the auto-generated marketing site.
- `packages/saasify-codegen`, `saasify-bulk-deploy`, `saasify-utils`: helpers.
- `docs/`: concepts and configuration (`configuration.md`, `pricing.md`, `openapi.md`, `serverless.md`, `marketing.md`, `env-vars-and-secrets.md`, `use-cases.md`, `examples.md`).
- `examples/`: example projects (for example `examples/typescript/imagemin`).

## How to help

1. For "how did Saasify do X", read the relevant doc in `docs/` and the matching package source, then explain it.
2. For reuse, point to the specific package and file, check its `package.json` for dependencies, and warn that the packages are unmaintained since 2022 (dependencies may be outdated or vulnerable).
3. For monetizing an API today, use Saasify's design (OpenAPI spec as source of truth, API keys, metered Stripe billing, generated docs/landing page) as a pattern, and suggest maintained alternatives the user can verify, instead of the dead platform.
