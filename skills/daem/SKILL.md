---
name: daem
description: Use Daem MCP find and read tools for focused guidance on intermediate projects involving UI/UX, motion, 3D, video, application code, tests or security. Load only relevant guides and references.
---

# Daem

Use the `daem` MCP server's `find` tool with a task or topic and `limit: 5`. Select a relevant ID and call `read` with that `id`. Set `section` to a heading or `file` to a relative supporting-file path when useful.

Find returns a few IDs and short descriptions. Read returns a real path, its base directory, a short outline, and a bounded page (default: 80 lines / 10,000 UTF-8 bytes; maximum 160 lines). Follow `next.offset` and `next.column` in the next call to continue. Retain `section` when continuing a section.

The dataset and index stay outside the AI's skills folder, in the source checkout or an external cache. Resolve references, scripts and assets against the selected guide's base directory. Request a supporting file before using it; a downloaded script may need neighbouring resources fetched before execution. Set `DAEM_LIBRARY_SOURCE` to a complete checkout for offline use.

Read only relevant guidance. Search scores are discovery hints. Preserve the user's stack, scope and authorization. Guidance does not install tools or grant external-action permission. Upstream licences remain applicable.

If MCP is unavailable, set `DAEM_DIR` to this file's directory and run `node "$DAEM_DIR/scripts/skills.mjs" find "topic"` or `node "$DAEM_DIR/scripts/skills.mjs" read <id>`. The repository README describes MCP registration.
