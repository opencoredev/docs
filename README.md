# OpenChat Docs (Mintlify)

Documentation site for OpenChat.

## Local development

Use the Mintlify CLI from the repo root:

```bash
bunx @mintlify/cli dev
```

## CI checks

This repo runs docs validation on pull requests and pushes to `main`:

- `mint validate`
- `mint broken-links`

Workflow file: `.github/workflows/docs-ci.yml`

## Auto-deploy setup (required)

Mintlify production deploys are driven by the Mintlify GitHub App, not by a CLI deploy command.

1. Open Mintlify dashboard Git settings.
2. Confirm connected repository is `opencoredev/docs`.
3. Install/authorize Mintlify GitHub App for the repo owner org.
4. Ensure deployment branch is `main`.
5. Push a commit to `main` and verify a deployment appears in Mintlify Deployments.

If autodeploy is still missing after these steps, use the Deploy button in Mintlify dashboard once to re-sync webhooks.

## References

- Mintlify GitHub integration: `https://www.mintlify.com/docs/deploy/github`
- Mintlify deployments: `https://www.mintlify.com/docs/deploy/deployments`
