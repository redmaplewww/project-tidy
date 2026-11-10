# project-tidy

A lightweight Codex skill for organizing project working files and historical versions into a searchable, recoverable archive.

[简体中文](README.md) · **English**

## Features

- Distinguishes versions from parallel alternatives; keeps a confirmed final version or, during iteration, the latest three version groups by default.
- Respects the project's existing authoritative documents, active dependencies, and archive rules; leaves uncertain files in place.
- Keeps the user-facing results area within three levels where practical, while preserving necessary engineering and archive structures.
- Records original paths, archive paths, keywords, and notes before moving files; does not delete or overwrite by default.
- Searches the index first, then relevant archived content as needed, and checks the source and its scope before using a result.

This is a set of instructions for an AI assistant, not a background service or an automatic cleanup program. Results depend on the model, available tools, and project materials. Installation does not start a file scan.

## Installation

Clone this repository into the Codex skills directory. macOS / Linux:

```bash
git clone https://github.com/redmaplewww/project-tidy.git ~/.codex/skills/project-tidy
```

Windows PowerShell:

```powershell
git clone https://github.com/redmaplewww/project-tidy.git "$env:USERPROFILE\.codex\skills\project-tidy"
```

If you use a custom `CODEX_HOME`, put the repository under its `skills/project-tidy` directory. Resolve any existing directory conflict before cloning to avoid overwriting another skill.

## Usage

Ask in a project conversation:

```text
Use $project-tidy to organize the current project. Check references first and make the archive recoverable.
```

You can also request a preview, search historical material, or restore specific archived files. The skill reads the [retrieval reference](references/retrieval.md) when needed; an indexed historical document is not automatically a current source of truth.

## Limitations

- No guarantee is made that every natural-language query will retrieve all relevant files. Check source material and report unsearched formats or scopes.
- An archive is not an independent backup; arrange backups separately.
- When strict reversibility is requested, the instructions call for recording original paths and checking per-file hashes. Verify the actual result after each cleanup.

## License

[MIT](LICENSE)
