# Agent Compatibility

Compatible with the [skills.sh](https://skills.sh) open agent ecosystem.

## Installation

### Vercel Skills (npx)

```bash
# Install for all supported agents
npx skills add hyperb1iss/hyperdroid-skill

# Install for specific agent
npx skills add hyperb1iss/hyperdroid-skill -a cursor
npx skills add hyperb1iss/hyperdroid-skill -a copilot
npx skills add hyperb1iss/hyperdroid-skill -a codex
npx skills add hyperb1iss/hyperdroid-skill -a gemini

# List available skills
npx skills add hyperb1iss/hyperdroid-skill --list
```

### Claude Code Plugin

```bash
# Add the marketplace
/plugin marketplace add hyperb1iss/hyperdroid-skill

# Install the plugin
/plugin install hyperdroid
```

## Supported Agents

- **claude-code** — Anthropic's Claude Code CLI
- **cursor** — Cursor AI editor
- **copilot** — GitHub Copilot
- **codex** — OpenAI Codex CLI
- **gemini** — Google Gemini CLI
- **amp** — Amp agent
- **opencode** — Opencode agent
- **antigravity** — Antigravity agent

## Skills Provided

| Skill | Description |
| --- | --- |
| `android` | Device mastery via ADB — debugging, shell, app management, UI automation |
| `android-bootloader` | Fastboot, partition flashing, bootloader unlocking, recovery, root |
| `android-build` | Gradle CLI, SDK tools, AOSP build system, kernels, device trees |
| `lineageos` | Custom ROM development — breakfast/brunch, repopick, Gerrit workflow |

## Skill Triggers

### android

Activates when the user mentions:

- `adb`, logcat, shell commands, device debugging
- App installation, screenshots, UI automation
- dumpsys, getprop, system inspection
- Crash analysis, memory profiling, ANR traces

### android-bootloader

Activates when the user mentions:

- `fastboot`, flash, partition management
- Bootloader unlock, recovery mode, TWRP
- Magisk, KernelSU, root operations
- A/B slots, dynamic partitions

### android-build

Activates when the user mentions:

- Gradle build, assemble, lint, test tasks
- AOSP, envsetup, lunch, mka
- SDK manager, emulator, AVD
- Device trees, kernel compilation

### lineageos

Activates when the user mentions:

- LineageOS, breakfast, brunch, mka bacon
- repopick, Gerrit, code review
- Vendor blobs, extract-files.sh
- Local manifests, device porting

## Agent Registry

### Device Interaction (`hyperdroid:android`)

- `hyperdroid:crash-analyzer` — Autonomous crash investigation: collects logs, tombstones, ANR traces, provides root cause diagnosis

## Directory Structure

```
skills/
├── android/
│   ├── SKILL.md              # Device mastery — ADB, debugging, system inspection
│   └── references/
│       └── deep-dive.md      # Advanced ADB techniques
├── android-bootloader/
│   ├── SKILL.md              # Fastboot, flashing, recovery, root
│   └── references/
│       └── partitions.md     # Partition layouts & A/B mechanics
├── android-build/
│   ├── SKILL.md              # Gradle CLI, SDK tools, AOSP builds
│   └── references/
│       ├── aosp.md           # AOSP build system deep dive
│       └── lineageos.md      # LineageOS build specifics
└── lineageos/
    ├── SKILL.md              # Custom ROM development workflow
    └── references/
        └── gerrit-workflow.md  # Gerrit contribution process
```

## Stats

| Metric | Count |
| --- | --- |
| Skills | 4 |
| Agents | 1 |
| Skill Lines | ~3,200 |

## Usage

Invoke skills with `/hyperdroid-skill:<skill>`:

```bash
/hyperdroid-skill:android              # Device interaction guidance
/hyperdroid-skill:android-bootloader   # Fastboot and recovery
/hyperdroid-skill:android-build        # Build system expertise
/hyperdroid-skill:lineageos            # Custom ROM development
```

Agents are invoked via the Task tool:

```
Task(subagent_type="hyperdroid:crash-analyzer", prompt="My app crashes on startup...")
```

## License

MIT
