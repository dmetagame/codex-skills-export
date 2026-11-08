# Codex Skills Export

Portable copy of the installed Codex skill folders for transfer to another agent.

## Contents

- `skills/user/`: 378 current user-level skills from `.agents/skills`.
- `skills/system/`: 5 bundled Codex system skills.
- `skills/plugins/`: 66 skill folders found in Codex plugin caches. Plugin tools and connections are not included.
- `skills/local-backup/`: 44 skills from the existing local backup at `data/skills`, kept separate because versions may overlap.
- `SKILL_INDEX.md`: human-readable inventory.
- `MANIFEST.json`: file paths, sizes, and SHA-256 hashes for integrity checks.

## Import into another agent

Give the agent the repository or archive and ask it to extract each directory containing `SKILL.md`, keeping the sibling references and assets in that directory. Have it use its supported skill import mechanism and adapt tool-specific steps to the tools it actually has. The skill files provide instructions; they do not transfer Codex tools, credentials, or service connections.

Some entries are third-party or platform-provided. Their original license and attribution files are preserved where present; follow those terms when reusing or redistributing a skill.

## Verify the payload

Compare file hashes against `MANIFEST.json`. The manifest records documentation metadata and content hashes only; it contains no absolute source paths or credentials.
