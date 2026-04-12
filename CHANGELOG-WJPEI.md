# CHANGELOG-WJPEI

## [v2026.4.11] - 2026-04-12

### Sync Information
- **Upstream Tag:** `v2026.4.11`
- **Origin Main SHA:** `e7d11f6c33e223a0dd8a21cfe01076bd76cef87a`
- **Upstream Main SHA:** `c9e12cbd32ee09e09a9eeb6cf0ed5ace4f89e867`

### Custom Commits
- **01e6974a98** - `wjpei: document tag tracking branch requirement`
  - Updates `GEMINI.md` to specify the creation of `<TAG>-wjpei` tracking branches.
- **cb194b665a** - `wjpei: document deployment workflow in GEMINI.md`
  - Adds the deployment workflow for `wjpei-deploy` and `kiiru-deploy` branches.

## [v2026.3.24] - 2026-03-28

### Sync Information
- **Upstream Tag:** `v2026.3.24`
- **Origin Main SHA:** `e7d11f6c33e223a0dd8a21cfe01076bd76cef87a`
- **Upstream Main SHA:** `269f461b2ea1dd7168b30887dabbfd0c6a0622d9`

### Custom Commits
- **17255a4606** - `wjpei: add host.docker.internal to gateway extra_hosts`
  - Adds `host.docker.internal` to the gateway service in `docker-compose.yml` to allow the gateway to access the host machine.
- **ebb0d7348f** - `wjpei: add DOCKER_UID/DOCKER_GID support to docker-compose`
  - Adds support for `DOCKER_UID` and `DOCKER_GID` environment variables in `docker-compose.yml` to ensure files created by the container have the correct ownership.
- **0dd8f9f4c5** - `wjpei: add GEMINI.md and CHANGELOG-WJPEI.md for custom change tracking`
  - Initializes `GEMINI.md` for project context and `CHANGELOG-WJPEI.md` for tracking custom modifications.
