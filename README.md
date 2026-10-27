# Avatar — Virtual World Test

The game archive is stored in `my-virtual-world_v10_cloudflare_online.zip`. The GitHub Actions workflow extracts it and deploys the Worker plus static game assets through Wrangler.

## One-time setup required

In GitHub, open **Settings → Secrets and variables → Actions → New repository secret** and add:

- `CLOUDFLARE_API_TOKEN`: a Cloudflare API token allowed to deploy Workers.
- `CLOUDFLARE_ACCOUNT_ID`: your Cloudflare account ID.

Then open **Actions → Deploy Avatar test world → Run workflow**. The workflow uses a separate Worker name (`avatar-virtual-world-test`) so it does not overwrite the existing `damp-shadow-03ce` Worker.

## Important

The live game URL will only exist after a successful deployment. The workflow has been added, but it cannot deploy until the two Cloudflare secrets are configured. The online multiplayer prototype still needs a two-account test after deployment.
