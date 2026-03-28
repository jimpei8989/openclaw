# Gemini CLI Context

## Project Goals
- Track custom modifications relative to the official `openclaw/openclaw` repository.
- Maintain a persistent development branch: `wjpei-dev`.
- Regularly synchronize with stable releases from `upstream`.

## Git Configuration
- **Origin:** `git@github.com:jimpei8989/openclaw.git` (User's fork)
- **Upstream:** `https://github.com/openclaw/openclaw.git` (Official repository)

## Workflow Strategy
- **Development Branch:** `wjpei-dev` is the primary branch for custom changes.
- **Sync Strategy:** Merge stable release tags from `upstream` into the development flow.
- **Current Baseline:** Stable release `v2026.3.24`.
- **Commit Convention:** All custom commits must start with the prefix `wjpei: ` (e.g., `wjpei: add custom tracking files`).
- **Change Tracking:** Maintain `CHANGELOG-WJPEI.md` as part of the merge process. 
  - Record the `upstream` stable release tag being targeted.
  - Include the latest SHAs from both `origin/main` and `upstream` for auditability.
  - For each custom commit in `wjpei-dev`, record the SHA, title, and a concise summary.
  - Update the changelog file consistently with every merge commit.

## Deployment Workflow
- **Deployment Branches:** `wjpei-deploy` and `kiiru-deploy` are specialized branches containing environment-specific changes (e.g., `.env` files).
- **Base Branch:** Both deployment branches are based off `wjpei-dev`.
- **Post-Merge Actions:** After `wjpei-dev` is updated (via merge from `upstream`), the following deployment steps are required upon user request:
  - Rebase or merge `wjpei-dev` into `wjpei-deploy`.
  - Rebase or merge `wjpei-dev` into `kiiru-deploy`.
  - Ensure any environment-specific overrides in these branches are preserved.

