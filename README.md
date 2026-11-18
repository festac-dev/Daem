# Daem

A focused collection of practical skills for building intermediate projects: motion, UI/UX, 3D, video and demos, secure coding, authorized pentesting, testing, documentation and deployment.

## Install globally

Install the small Daem entrypoint for Codex, Claude Code and OpenCode across all your projects:

```sh
npx skills add festac-dev/Daem --skill daem --agent codex claude-code opencode -g -y --copy
```

Requires Node.js 22.20+ and Git. `-g` installs globally so skills are available across projects. To install for only your current AI tool, choose its agent name:

```sh
npx skills add festac-dev/Daem --skill daem -a opencode -g -y --copy
```

Use `codex`, `claude-code`, or `opencode`. Skills are stored in locations supported by the selected agent: Codex and OpenCode can use `~/.agents/skills/`; Claude Code uses `~/.claude/skills/`. The documented commands use `--copy` to install actual skill files.

A skill supplies instructions. Tools, APIs and application dependencies mentioned by it must be available when the task needs them.

## Find and read over MCP

The AI discovers one small entrypoint. The 36 guides, assets, licences and search index stay outside the agent's skills folders, in this checkout or an external cache. MCP exposes `find` and `read`; search returns a few matches and read returns bounded pages with continuation positions.

Register MCP globally from a checkout:

```sh
node scripts/setup-mcp.mjs --all
```

Or configure an MCP server using `node ~/.agents/skills/daem/scripts/mcp-server.mjs` (Claude's copied entrypoint is under `~/.claude/skills/daem`). First search fetches the pinned index into `~/.cache/festac-skills/`; selected guides and supporting files are fetched on demand. Set `DAEM_LIBRARY_SOURCE` to a complete checkout for offline use.

The CLI uses the same engine:

```sh
node ~/.agents/skills/daem/scripts/skills.mjs find "motion video" --limit 3
node ~/.agents/skills/daem/scripts/skills.mjs read daem-ui-ux
```

## Included guides

| Skill | Use for |
|---|---|
| [daem-motion](skills/daem-motion/SKILL.md) | Motion graphics, animation and video workflows |
| [daem-motion-direction](skills/daem-motion-direction/SKILL.md) | Motion graphics direction and frame-by-frame review |
| [daem-unslop](skills/daem-unslop/SKILL.md) | Improve AI-generated interface design |
| [daem-3d-scenes](skills/daem-3d-scenes/SKILL.md) | Build and organize Three.js scenes |
| [daem-3d-animation](skills/daem-3d-animation/SKILL.md) | Animate 3D scenes |
| [daem-3d-materials](skills/daem-3d-materials/SKILL.md) | Materials and shaders |
| [daem-3d-assets](skills/daem-3d-assets/SKILL.md) | Load 3D models and textures |
| [daem-3d-rendering](skills/daem-3d-rendering/SKILL.md) | Rendering and performance |
| [daem-video](skills/daem-video/SKILL.md) | Cinematic product videos and shot planning |
| [daem-demo-capture](skills/daem-demo-capture/SKILL.md) | Capture product demo videos |
| [daem-demo-storytelling](skills/daem-demo-storytelling/SKILL.md) | Narrated product demo videos |
| [daem-frontend-design](skills/daem-frontend-design/SKILL.md) | Distinctive frontend visual design |
| [daem-ui-polish](skills/daem-ui-polish/SKILL.md) | UI typography, spacing and interaction polish |
| [daem-accessibility](skills/daem-accessibility/SKILL.md) | Accessible UI and WCAG checks |
| [daem-requirements](skills/daem-requirements/SKILL.md) | Turn a feature brief into requirements |
| [daem-architecture](skills/daem-architecture/SKILL.md) | Application architecture and tradeoffs |
| [daem-fullstack](skills/daem-fullstack/SKILL.md) | Deliver complete frontend and backend features |
| [daem-api-design](skills/daem-api-design/SKILL.md) | API contracts and error handling |
| [daem-database](skills/daem-database/SKILL.md) | Queries, schema and database performance |
| [daem-secure-coding](skills/daem-secure-coding/SKILL.md) | Secure implementation and OWASP checks |
| [daem-security-review](skills/daem-security-review/SKILL.md) | Review code and infrastructure security |
| [daem-pentest](skills/daem-pentest/SKILL.md) | Plan and conduct authorized penetration tests |
| [daem-testing](skills/daem-testing/SKILL.md) | Test strategy and meaningful coverage |
| [daem-browser-testing](skills/daem-browser-testing/SKILL.md) | Browser tests and debugging |
| [daem-deployment](skills/daem-deployment/SKILL.md) | Build, deployment and operational checks |
| [daem-documentation](skills/daem-documentation/SKILL.md) | Maintain useful technical documentation |
| [daem-code-review](skills/daem-code-review/SKILL.md) | Review implementation changes |
| [daem-typescript](skills/daem-typescript/SKILL.md) | TypeScript implementation and type design |
| [daem-debugging](skills/daem-debugging/SKILL.md) | Find root causes before changing code |
| [daem-verification](skills/daem-verification/SKILL.md) | Verify changes before reporting completion |
| [daem-ui-ux](skills/daem-ui-ux/SKILL.md) | UI/UX design system, styles and practical recommendations |
| [daem-design-engineering](skills/daem-design-engineering/SKILL.md) | Implement refined interactions and interfaces |
| [daem-animation-vocabulary](skills/daem-animation-vocabulary/SKILL.md) | Specify animation in concrete terms |
| [daem-animation-review](skills/daem-animation-review/SKILL.md) | Review animation timing and interaction |
| [daem-domain-modeling](skills/daem-domain-modeling/SKILL.md) | Model application concepts and boundaries |
| [daem-find-skills](skills/daem-find-skills/SKILL.md) | Find additional task-specific skills |

## Licences

Imported skills retain their upstream licences and attribution. See [NOTICE.md](NOTICE.md), [SOURCES.json](SOURCES.json), and the licence files within each skill. The collection does not establish permission to test someone else's systems; pentesting guidance applies within the user's authorized scope.
