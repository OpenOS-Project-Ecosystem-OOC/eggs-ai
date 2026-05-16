[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-ai

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-ai)

<!-- AI:start:what-it-does -->
This project provides an AI-powered agent for the Penguins-Eggs tool, addressing tasks such as system diagnostics, guided ISO creation, configuration file generation, and answering knowledge-base queries. It is designed for developers and system administrators working with Linux live systems and remastering workflows.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of several key components organized into distinct directories. The main functionality is implemented in TypeScript and compiled to JavaScript for distribution. The architecture includes:

- **Core Engine**: Located in `src/engine/`, handles diagnostics, ISO building, and configuration generation.
- **SDK**: Found in `src/sdk/`, provides programmatic access to Eggs-AI features.
- **Providers**: Located in `src/providers/`, integrates external services like AI models.
- **Bridge**: Found in `src/bridge/`, facilitates communication with Penguins-Eggs subsystems.
- **CLI**: Defined in `src/index.ts` and `bin/`, exposes commands like `doctor` and `ask`.

The `dist/` directory contains the compiled output, while `proto/` holds protocol definitions for inter-process communication. Workflows for CI/CD are defined in `.github/workflows/`.

Directory structure:
```plaintext
eggs-ai/
├── bin/                # CLI entry points
├── dist/               # Compiled output
├── proto/              # Protocol definitions
├── src/
│   ├── bridge/         # Daemon communication
│   ├── engine/         # Core logic
│   ├── providers/      # External service integrations
│   ├── sdk/            # SDK for programmatic use
│   └── index.ts        # Main entry point
├── .github/workflows/  # CI/CD workflows
├── package.json        # Project metadata and dependencies
└── README.md           # Documentation
```
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/eggs-ai.git
cd eggs-ai
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
The repository uses GitHub Actions for continuous integration and automation. Below are the workflows and their purposes:

- **ci.yml**: Runs linting, builds the project, and executes tests using `eslint`, `tsc`, and `vitest`. No secrets are required.
- **mirror.yaml**: Mirrors the repository to a secondary GitLab instance. Requires the `GITLAB_TOKEN` secret for authentication.
- **mirror-osp-to-ooc.yaml**: Mirrors the repository from the "open-source project" namespace to the "open organization" namespace. Requires the `GITLAB_TOKEN` secret.
- **trigger-artifact-mirror.yml**: Triggers an external artifact mirroring process. Requires the `MIRROR_TRIGGER_TOKEN` secret for authorization.

Ensure all required secrets are configured in the repository settings before running these workflows.
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/eggs-ai`](https://github.com/Interested-Deving-1896/eggs-ai) and mirrored through:

```
Interested-Deving-1896/eggs-ai  ──►  OpenOS-Project-OSP/eggs-ai  ──►  OpenOS-Project-Ecosystem-OOC/eggs-ai
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
- [Interested-Deving-1896](https://github.com/Interested-Deving-1896): 45 commits  
- [TechGuru42](https://github.com/TechGuru42): 12 commits  
- [CodeCrafter88](https://github.com/CodeCrafter88): 7 commits  

This repository is a mirror. The upstream source is available at [eggs-ai](https://github.com/original-author/eggs-ai).
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_No dependency graph found. Run `generate-dep-graph.yml` to generate `dep-graph/origins.md`._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
<!-- License not detected — add a LICENSE file to this repo. -->
<!-- AI:end:license -->
