# Daem

A focused collection of practical skills for building intermediate projects: motion, UI/UX, 3D, video and demos, secure coding, authorized pentesting, testing, documentation and deployment.

## Install for your AI app

These public commands work for anyone. Choose the app you use. `-g` makes the entrypoint available across projects; the second command registers the MCP server in that app's user configuration. Node.js 22.20+ and Git are required.

### Codex

```sh
npx skills add festac-dev/Daem --skill daem --agent codex -g -y --copy
node "$HOME/.agents/skills/daem/scripts/setup-mcp.mjs" --codex
```

### Claude Code

```sh
npx skills add festac-dev/Daem --skill daem --agent claude-code -g -y --copy
node "$HOME/.claude/skills/daem/scripts/setup-mcp.mjs" --claude-code
```

### OpenCode

```sh
npx skills add festac-dev/Daem --skill daem --agent opencode -g -y --copy
node "$HOME/.agents/skills/daem/scripts/setup-mcp.mjs" --opencode
```

### All three apps

```sh
npx skills add festac-dev/Daem --skill daem --agent codex claude-code opencode -g -y --copy
node "$HOME/.agents/skills/daem/scripts/setup-mcp.mjs" --all
```

The installer uses each person's home directory. MCP registration preserves other servers and backs up changed configuration files. Open a fresh agent session after setup.

## Read skills through MCP

The AI's skill folders contain only a small entrypoint and its runtime scripts. The dataset and index stay outside those folders. MCP `find` returns a few IDs and short descriptions; `read` loads a selected skill, section, or supporting file in bounded pages. Default: 80 lines, with at most 10,000 UTF-8 content bytes; maximum: 160 lines. Follow the returned `next.offset` and `next.column` to continue.

On first search, the index is cached under `~/.cache/festac-skills/` (or `XDG_CACHE_HOME`). Selected skills and files are cached there on demand. The full catalogue is never inserted into AI context automatically.

For offline use, clone the repository outside your agent's skills folder. Register MCP from the checkout:

```sh
git clone https://github.com/festac-dev/Daem.git
cd Daem
node scripts/setup-mcp.mjs --all
```

The setup script finds the checkout on the current machine. `DAEM_LIBRARY_SOURCE` can also select a complete local dataset. Supporting scripts may require neighbouring resources before execution.

## Included skills

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
