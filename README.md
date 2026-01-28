<h1 align="center">
  🤖 hyperdroid-skill
</h1>

<p align="center">
  <strong>Master Android Development from App to ROM</strong><br>
  <sub>ADB wizardry • Fastboot sorcery • Custom ROM alchemy</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Skills-4_Domains-e135ff?style=for-the-badge&logo=android&logoColor=white" alt="4 Skills">
  <img src="https://img.shields.io/badge/Agent-Crash_Analyzer-80ffea?style=for-the-badge&logo=robot&logoColor=black" alt="1 Agent">
  <img src="https://img.shields.io/badge/Claude_Code-Plugin-ff6ac1?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/skills.sh-Compatible-f1fa8c?style=for-the-badge&logo=npm&logoColor=black" alt="skills.sh">
</p>

<p align="center">
  <a href="https://github.com/hyperb1iss/hyperdroid-skill/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/hyperb1iss/hyperdroid-skill?style=flat-square&logo=opensourceinitiative&logoColor=white" alt="License">
  </a>
</p>

<p align="center">
  <a href="#-what-this-is">What This Is</a> •
  <a href="#-skills">Skills</a> •
  <a href="#-agents">Agents</a> •
  <a href="#-installation">Installation</a> •
  <a href="#-sota-knowledge">SOTA Knowledge</a>
</p>

---

## 💎 What This Is

**hyperdroid-skill** is an elite Claude Code plugin for Android development—from debugging a misbehaving app to building entire custom ROMs. Whether you're a hobbyist flasher or a full-time ROM maintainer, these skills have you covered.

Instead of digging through Stack Overflow and XDA threads, get **domain expertise** directly:

- A **device debugger** who knows logcat, tombstones, and ANR traces inside-out
- A **fastboot specialist** who handles A/B slots, dynamic partitions, and brick prevention
- A **build engineer** who speaks Gradle, Soong, and `lunch` fluently
- A **LineageOS contributor** who knows Gerrit, repopick, and breakfast by heart

Works with Claude Code and any agent supporting the plugin ecosystem.

## 🔮 Skills

Skills are contextual knowledge bundles that auto-activate when relevant. Ask about "adb logcat"? The android skill loads. Mention "flash boot image"? Bootloader skill activates.

| Skill | Domain | Triggers |
|-------|--------|----------|
| `android` | Device Mastery | ADB, logcat, shell, app management, UI automation, debugging |
| `android-bootloader` | Danger Zone | Fastboot, partitions, A/B slots, recovery, Magisk, unlocking |
| `android-build` | Build Systems | Gradle CLI, SDK manager, AOSP envsetup/lunch/m, kernels |
| `lineageos` | Custom ROMs | breakfast/brunch, repopick, Gerrit, vendor blobs, porting |

### 🎯 `android` — Device Mastery

Everything about interacting with Android devices via ADB:

- **Connection** — USB, wireless (`adb tcpip`), multi-device targeting
- **Shell** — Commands, root access, file push/pull, port forwarding
- **App Management** — Install, uninstall, start/stop activities, permissions, intents
- **UI Automation** — Tap, swipe, text input, screenshots, screen recording
- **Debugging** — Logcat filtering, crash analysis, memory profiling, strict mode
- **System Inspection** — dumpsys, getprop, /proc exploration, service calls

### ⚠️ `android-bootloader` — Danger Zone

Fastboot and bootloader operations with appropriate safety warnings:

- **Fastboot Commands** — Flash, erase, boot, getvar, reboot modes
- **Bootloader State** — Unlock, lock, OEM commands, critical partitions
- **A/B Partitions** — Slot switching, dynamic partitions (super), metadata
- **Recovery** — TWRP, stock recovery, sideload, OTA survival
- **Root** — Magisk installation, boot image patching, module management
- **Brick Prevention** — Backup strategies, critical partition protection, recovery paths

### 🔧 `android-build` — Build Systems

Both app and ROM building expertise:

- **Gradle CLI** — Tasks, variants, dependency resolution, build optimization
- **SDK Tools** — sdkmanager, avdmanager, emulator management
- **AOSP Build** — envsetup.sh, lunch targets, m/mm/mmm, ninja
- **Device Trees** — Makefile structure, BoardConfig, device props
- **Kernel Building** — Defconfig, cross-compilation, module building

### 🌙 `lineageos` — Custom ROM Development

LineageOS-specific development workflows:

- **Source Management** — repo init/sync, local manifests, breakfast
- **Building** — brunch, target selection, signed builds
- **Gerrit Workflow** — repopick, topic branches, code review
- **Vendor Blobs** — extract-files.sh, proprietary-files.txt, TheMuppets
- **Device Porting** — Common trees, inheritance, bring-up process
- **Contributing** — Commit style, Gerrit etiquette, LineageOS standards

## 🦋 Agents

Agents are invoked via the Task tool with `subagent_type="hyperdroid:agent-name"`.

| Agent | Specialty |
|-------|-----------|
| `hyperdroid:crash-analyzer` | Autonomous crash investigation — collects logs, tombstones, ANR traces, analyzes native crashes, provides root cause diagnosis |

### Crash Analyzer

When your app or device is misbehaving, this agent:

1. Collects relevant logcat output with intelligent filtering
2. Retrieves tombstones and native crash dumps
3. Parses ANR traces and identifies blocked threads
4. Correlates crashes with recent changes
5. Provides actionable diagnosis and fix suggestions

```
> My app keeps crashing on startup
[crash-analyzer agent activates, gathers evidence, returns diagnosis]
```

## ⚡ Installation

### Vercel Skills (npx)

```bash
# Install for all supported agents
npx skills add hyperb1iss/hyperdroid-skill

# Install for a specific agent
npx skills add hyperb1iss/hyperdroid-skill -a cursor
npx skills add hyperb1iss/hyperdroid-skill -a copilot
npx skills add hyperb1iss/hyperdroid-skill -a codex
npx skills add hyperb1iss/hyperdroid-skill -a gemini
```

### Claude Code Plugin

```bash
# Add the marketplace
/plugin marketplace add hyperb1iss/hyperdroid-skill

# Install the plugin
/plugin install hyperdroid
```

### Manual

```bash
git clone https://github.com/hyperb1iss/hyperdroid-skill.git
ln -s $(pwd)/hyperdroid-skill ~/.claude/plugins/hyperdroid-skill
```

### Test Locally

```bash
claude --plugin-dir ./hyperdroid-skill
```

### Compatibility

| Platform | Install Method |
|----------|----------------|
| **Claude Code** | `/plugin marketplace add hyperb1iss/hyperdroid-skill` |
| **Vercel Skills** | `npx skills add hyperb1iss/hyperdroid-skill` |
| **Codex CLI** | `npx skills add hyperb1iss/hyperdroid-skill -a codex` |
| **Cursor** | `npx skills add hyperb1iss/hyperdroid-skill -a cursor` |
| **GitHub Copilot** | `npx skills add hyperb1iss/hyperdroid-skill -a copilot` |
| **Gemini CLI** | `npx skills add hyperb1iss/hyperdroid-skill -a gemini` |
| **Amp** | `npx skills add hyperb1iss/hyperdroid-skill -a amp` |
| **Opencode** | `npx skills add hyperb1iss/hyperdroid-skill -a opencode` |

## 🎯 Usage

Skills activate automatically based on context:

```
> Connect to my Android device wirelessly
[android skill activates — guides through adb tcpip setup]

> Flash the custom boot image I just built
[android-bootloader skill activates — provides safe fastboot workflow]

> Build LineageOS for my Pixel 8
[lineageos skill activates — walks through breakfast/brunch process]

> Why does my app crash when rotating the screen?
[crash-analyzer agent investigates lifecycle issues]
```

Or invoke directly:

```bash
/hyperdroid-skill:android              # Device interaction guidance
/hyperdroid-skill:android-bootloader   # Fastboot and recovery
/hyperdroid-skill:android-build        # Build system expertise
/hyperdroid-skill:lineageos            # Custom ROM development
```

## 🧪 SOTA Knowledge

Every skill is enhanced with modern Android development knowledge (2024-2026):

### Device Interaction

- **Wireless ADB** — Direct WiFi pairing (Android 11+), no USB required
- **scrcpy Integration** — Screen mirroring, wireless debugging, input injection
- **Multi-Device** — Serial targeting, parallel operations, device farms
- **Automation** — UI Automator 2, Espresso test orchestration, macro recording

### Build Systems

- **Gradle 8.x** — Configuration cache, build scans, dependency verification
- **AGP 8.x** — Baseline profiles, R8 full mode, app bundles
- **Kotlin DSL** — Type-safe build scripts, convention plugins
- **Version Catalogs** — Centralized dependency management (libs.versions.toml)

### AOSP/LineageOS

- **Soong** — Blueprint files, Android.bp, module types
- **Bazel Migration** — Mixed Soong/Bazel builds, aquery debugging
- **GKI 2.0** — Generic Kernel Image, DLKM modules, vendor_dlkm
- **Treble** — HIDL/AIDL interfaces, vendor partitions, GSI compatibility
- **Dynamic Partitions** — super partition, resize operations, snapshot merges

### Security & Root

- **Magisk 26+** — Zygisk, DenyList, module development
- **KernelSU** — Kernel-level root, module compatibility
- **SafetyNet/Play Integrity** — Attestation, device integrity, hiding root
- **SELinux** — Policy debugging, permissive domains, audit2allow

### Debugging

- **Perfetto** — System tracing, custom trace points, SQL analysis
- **Simpleperf** — CPU profiling, flame graphs, hardware PMU
- **Memory Profiler** — Heap dumps, allocation tracking, leak detection
- **Network Profiler** — Traffic inspection, certificate pinning bypass

## 📦 Structure

```
hyperdroid-skill/
├── .claude-plugin/
│   ├── plugin.json              # Claude Code manifest
│   └── marketplace.json         # skills.sh distribution index
├── AGENTS.md                    # Agent compatibility registry
├── skills/
│   ├── android/
│   │   ├── SKILL.md             # Quick reference + triggers
│   │   └── references/          # Deep documentation
│   │       └── deep-dive.md     # Advanced ADB techniques
│   ├── android-bootloader/
│   │   ├── SKILL.md
│   │   └── references/
│   │       └── partitions.md    # Partition layouts & safety
│   ├── android-build/
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── aosp.md          # AOSP build deep dive
│   │       └── lineageos.md     # LineageOS specifics
│   └── lineageos/
│       ├── SKILL.md
│       └── references/
│           └── gerrit-workflow.md
├── agents/
│   └── crash-analyzer.md        # Autonomous crash investigation
├── research/                    # Development references (not in plugin)
├── Makefile                     # Lint, format, validate
└── README.md
```

## 🔧 Development

```bash
# Clone
git clone https://github.com/hyperb1iss/hyperdroid-skill.git
cd hyperdroid-skill

# Lint & format
make lint
make format

# Validate structure
make check

# Show stats
make stats

# Test locally
claude --plugin-dir .
```

## 💜 Philosophy

These skills embody the Android power-user methodology:

| Principle | What It Means |
|-----------|---------------|
| **Know the internals** | Understanding dumpsys, getprop, and /proc makes you dangerous |
| **Respect the danger** | Bootloader operations get explicit warnings — we don't brick devices |
| **Build from source** | Whether app or ROM, know your build system inside-out |
| **Debug systematically** | Logcat + tombstones + ANR traces = root cause, not guesswork |
| **Give back** | LineageOS thrives on contributors — learn the Gerrit workflow |

## 📚 Reference Materials

The `research/` directory contains extensive reference documentation used during skill development:

- **ADB mastery** — Every flag, every trick
- **Fastboot internals** — Partition tables, A/B mechanics
- **AOSP build system** — Soong, ninja, make
- **Kernel building** — Defconfigs, modules, GKI
- **Debugging tools** — Perfetto, simpleperf, memory analysis

## License

Licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

<p align="center">
  <a href="https://github.com/hyperb1iss/hyperdroid-skill">
    <img src="https://img.shields.io/github/stars/hyperb1iss/hyperdroid-skill?style=social" alt="Star on GitHub">
  </a>
  &nbsp;&nbsp;
  <a href="https://ko-fi.com/hyperb1iss">
    <img src="https://img.shields.io/badge/Ko--fi-Support%20Development-ff5e5b?logo=ko-fi&logoColor=white" alt="Ko-fi">
  </a>
</p>

<p align="center">
  <a href="https://github.com/hyperb1iss">
    <img src="https://img.shields.io/badge/GitHub-hyperb1iss-181717?style=for-the-badge&logo=github" alt="GitHub">
  </a>
  <a href="https://bsky.app/profile/hyperbliss.tech">
    <img src="https://img.shields.io/badge/Bluesky-@hyperbliss.tech-1185fe?style=for-the-badge&logo=bluesky" alt="Bluesky">
  </a>
</p>

<p align="center">
  <sub>
    If this helps you master Android development, give us a ⭐ or <a href="https://ko-fi.com/hyperb1iss">support the project</a>
    <br><br>
    ✦ Built with obsession by <a href="https://hyperbliss.tech"><strong>Hyperbliss Technologies</strong></a> ✦
  </sub>
</p>
