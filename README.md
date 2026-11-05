# Ruby's Built-in Repository

A fan-made package repository by WeirdMM for Ruby, the package manager for [WinterX](https://github.com/UltraFEmotes/WinterX). Published experimental packages: **Animaper, ColoredBar and SnowyHome**.

## Add to Ruby

WinterX includes a local copy as its built-in source. To add this hosted copy as a separate source, use the Sources tab in Ruby and enter:

`https://raw.githubusercontent.com/UltraFEmotes/Ruby-Repo/main/index.json`

The hosted and local built-in sources contain the same packages, so adding both may show duplicates. Repository operations require the Mac.APK Ruby bridge. Rooted Android is not supported yet. [Join the WinterX Discord](https://discord.gg/4JTe27ZRNd).

## Animaper

Animaper adds eight home-screen page-swipe effects. Its implementation is built into compatible WinterX engines; the `.springys` archive provides metadata and selects that hook. Install it in Ruby, then choose an effect from Spring Settings → Animaper. Repository and Settings handling remain experimental. Native Animaper/ColoredBar marker changes do not need respring on compatible engines; engine upgrades require a deliberate full launcher reopen, not an in-place restart.

## ColoredBar

Choose presets or any six-digit RGB hex colour in **Spring Settings → ColoredBar**, with per-app exclusions. Updated engines cover Settings' separate loader and App Store's custom bar, and list dock apps such as Phone under Excluded Apps. Ruby is permanently excluded; its own red navigation and bottom tabs remain red without tweaks and in Safe Mode.

Basic ColoredBar behaviour was live-confirmed on Mac.APK. New coverage/branding fixes passed isolated packaged-engine checks but still need a live trial. Build the updated WinterX engine and fully reopen Spring: the `.springys` archive selects a compiled hook, not an engine upgrade. Exclusions and recovery remain experimental.

## SnowyHome 0.2.1

Icon packs, badge colours, icon corners and hidden icon labels, set in **Spring Settings → WINTERX TWEAKS → SnowyHome**. New in 0.2.1: when icon labels are hidden, Home icons move down to sit centred in their cells (dock icons stay put).

SnowyHome 0.2.1 is a source-backed Java/Dex code package (`winterx.springys/3`). It needs the new modular WinterX core with native packages, which hasn't been published yet; older engines list it but can't install it. Its full source is in `sources/snowyhome/`.

FreeMe, DockIn and SSH are unfinished here. Developer examples and the old test tweaks are deliberately excluded from this index.

## Building packages

Editable package files are in `sources/animaper/` and `sources/coloredbar/`. From a WinterX checkout, run:

```sh
python3 tools/springys_tool.py build /path/to/Ruby-Repo/sources/animaper /tmp/animaper.springys
python3 tools/springys_tool.py inspect /tmp/animaper.springys
python3 tools/springys_tool.py build /path/to/Ruby-Repo/sources/coloredbar /tmp/coloredbar.springys
python3 tools/springys_tool.py inspect /tmp/coloredbar.springys
```

The output must not already exist. See the [package guide](https://github.com/UltraFEmotes/WinterX/blob/main/docs/springys-format.md) and [repository guide](https://github.com/UltraFEmotes/WinterX/blob/main/docs/repository-design.md) for details. The archive hash in `index.json` must match the published file.

Original project files are available under the [MIT License](LICENSE); Spring and other third-party software and trademarks belong to their respective owners.
