# Ruby's Built-in Repository

A fan-made package repository by WeirdMM for Ruby, the package manager for [WinterX](https://github.com/UltraFEmotes/WinterX). Every package here is a source-backed Java/Dex code package (`winterx.springys/3`) and needs the modular WinterX core; see the [WinterX repository](https://github.com/UltraFEmotes/WinterX).

## Add to Ruby

WinterX includes a local copy of this repository as its built-in source, so you don't need to add anything. To add the hosted copy as a separate source, open the Sources tab in Ruby and enter:

`https://raw.githubusercontent.com/UltraFEmotes/Ruby-Repo/main/index.json`

The hosted and built-in sources contain the same packages, so adding both may show duplicates. Install a package in Ruby, then fully close Spring and start it again through WinterX to load it. Its settings are under **Spring Settings → WINTERX TWEAKS**. [Join the WinterX Discord](https://discord.gg/4JTe27ZRNd).

## Packages

| Package | Version | What it does |
| --- | --- | --- |
| Animaper | 0.2.0 | Eight Home page-swipe effects. |
| ColoredBar | 0.2.0 | Recolours app navigation bars (presets or any hex colour), with per-app exclusions. Ruby always stays red. |
| DockIn | 0.2.0 | Choose four to seven dock icons. |
| FreeMe | 0.2.0 | Keep gaps in the Home grid, move icons across pages and keep native folders. |
| Message+ | 0.2.0 | Settings inside Messages and JPEG photo-quality choices. Video sending and reactions are unfinished. |
| SnowyHome | 0.2.1 | Icon packs, badge colours, icon corners and hidden icon labels. When labels are hidden, Home icons move down to sit centred in their cells. |
| SSH | 0.2.0 | An SSH server for Spring. It stays stopped until you start it in its Settings page with a configured key. |
| **Gravity** | 0.1.0 | Shake the phone and the Home icons fall as solid tiles. They tumble, pile up the way the phone is tilted and land on the dock. Grab and throw them, swipe to other pages (each page falls when you reach it), and tap a loose icon to open its app. Shake again or press Home and they float back into place. Labels hide while icons are loose. |
| **Harlem Shake** | 0.1.1 | A remake of the 2013 meme tweak. Tap Do the Harlem Shake in its Settings page and Settings closes to Home: one icon dances alone, then at the drop every icon joins in with a random move until the song ends. The song isn't included. Put an MP3 of your own in `Android/data/com.guille.spring/files/harlemshake` and tap the song row, or it dances in silence. |

The full source of each package is in `sources/<name>/`.

## Building packages

From a WinterX checkout with a built core (see [making tweaks](https://github.com/UltraFEmotes/WinterX/blob/main/docs/making-tweaks.md)):

```sh
python3 extensions/build.py package /path/to/Ruby-Repo/sources/gravity /tmp/gravity.springys \
  --sdk out/core/winterx-native-api.jar --spring-api out/core/spring-api.jar
```

The archive hash in `index.json` must match the published file. See the [repository guide](https://github.com/UltraFEmotes/WinterX/blob/main/docs/repository-design.md) for the index format.

Original project files are available under the [MIT License](LICENSE). Spring and other third-party software and trademarks belong to their respective owners.
