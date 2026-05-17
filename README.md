[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-ai

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-ai)

<!-- AI:start:what-it-does -->
This project provides an AI-powered agent for the Penguins-Eggs tool, a Linux system utility for creating and managing live ISO images. It assists users with diagnostics, guided ISO building, configuration generation, and querying a knowledge base. It is designed for developers and system administrators working with Linux live systems and remastering tasks.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of several key components organized into a modular directory structure. The main entry point is `dist/index.js`, which serves as the runtime for the AI agent. The `bin/` directory contains executable scripts, including `eggs-ai` for CLI interactions and `eggs-ai-mcp` for the multi-channel processing server. The `src/` directory contains the TypeScript source code, organized into submodules such as `engine/` for core logic, `sdk/` for programmatic access, `providers/` for external integrations, and `bridge/` for communication with the Penguins-Eggs daemon. Protobuf definitions are stored in the `proto/` directory for inter-process communication. Build artifacts are output to the `dist/` directory. The project uses TypeScript for development, with build and test scripts defined in `package.json`.

```
.
├── bin/                  # CLI entry points
├── dist/                 # Compiled output
├── proto/                # Protobuf definitions
├── src/                  # TypeScript source code
│   ├── bridge/           # Daemon communication
│   ├── engine/           # Core logic
│   ├── providers/        # External integrations
│   └── sdk/              # Programmatic API
├── test/                 # Unit and integration tests
├── .github/              # GitHub workflows
├── examples/             # Example configurations and usage
├── Dockerfile            # Docker build configuration
├── docker-compose.yaml   # Docker Compose setup
├── package.json          # Project metadata and scripts
└── tsconfig.json         # TypeScript configuration
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
