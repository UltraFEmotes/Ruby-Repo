# Ruby's Built-in Repository

A fan-made package repository by WeirdMM for Ruby, the package manager for [WinterX](https://github.com/UltraFEmotes/WinterX). Animaper is currently the only package; more tweaks will come later.

## Add to Ruby

WinterX includes a local copy as its built-in source. To add this hosted copy as a separate source, use the Sources tab in Ruby and enter:

`https://raw.githubusercontent.com/UltraFEmotes/Ruby-Repo/main/index.json`

The hosted source and local built-in source contain the same package, so adding both may show a duplicate. Ruby repository operations currently require the Mac.APK Ruby bridge. Rooted Android is not supported yet.

## Animaper

Animaper adds eight home-screen page-swipe effects. Its implementation is built into compatible WinterX engines; the `.springys` archive provides metadata and selects that hook. Install it in Ruby, then choose an effect from Spring Settings → Animaper on a compatible WinterX build. Settings integration and repository handling are experimental. Some operations may restart Spring; Mac.APK can get stuck on its boot screen after a restart.

## Building packages

The editable package files are in `sources/animaper/`. From a WinterX checkout, run:

```sh
python3 tools/springys_tool.py build /path/to/Ruby-Repo/sources/animaper /tmp/animaper.springys
python3 tools/springys_tool.py inspect /tmp/animaper.springys
```

The output must not already exist. See the [package guide](https://github.com/UltraFEmotes/WinterX/blob/main/docs/springys-format.md) and [repository guide](https://github.com/UltraFEmotes/WinterX/blob/main/docs/repository-design.md) for details. The archive hash in `index.json` must match the published file.

Original project files are available under the [MIT License](LICENSE); Spring and other third-party software and trademarks belong to their respective owners.
