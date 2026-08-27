# OpenBoa Plugins

This repository is the OpenBoa plugin marketplace. It is a catalog, not a plugin source tree.

## Purpose

The marketplace lets a client discover a plugin and decide whether it may be installed. Each entry points to an exact source revision in the plugin's own repository. The catalog does not copy plugin code, embed evaluation scores, or restate client support claims.

## Current catalog

- Marketplace ID: `openboa-plugins`
- Display name: `OpenBoa Plugins`
- Entry: `hydra`
- Source: `openboa-ai/hydra` at commit `ee67fdc39d4f4faf12bd2de38c2cc45f2105875b`
- Installation: `NOT_AVAILABLE` while the Hydra `0.0.0` foundation is being reviewed

The pinned revision is a candidate source commit, not a public release claim. After the Hydra foundation is merged, update the entry to the exact reviewed `main` commit and only then change availability as part of a release decision.

## Ownership boundaries

- Hydra owns its package, product meaning, version, and release.
- Hydra Eval owns task definitions, runs, verifiers, results, and invalidation history.
- This repository owns catalog identity, source selectors, category, and installation availability.

Support status remains in Hydra's client matrix. Evaluation evidence remains in [Hydra Eval](https://github.com/openboa-ai/hydra-eval). If either source cannot be verified, the catalog entry must remain unavailable.

## Format

The catalog follows Codex's repository marketplace format at `.agents/plugins/marketplace.json`. Git-backed entries use a repository URL and a full commit SHA. The source is the Hydra repository root because the portable `plugin.json` is at that root. A future plugin in a subdirectory must use the documented `git-subdir` source instead of copying files here.

The [Codex plugin packaging guide](https://developers.openai.com/plugins/build/plugins) defines the marketplace fields. The [Agent Plugins specification](https://agent-plugins.org/specification) defines the package format itself; it does not define a marketplace.
