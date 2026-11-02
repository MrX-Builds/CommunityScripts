# VisageStashLink

Small independent companion UI plugin for Visage.

## With appreciation for Visage

VisageStashLink is intentionally a very small companion. **Visage is the
remarkable project doing the important work.** CC1234 (`@cc1234475`) created
the facial-recognition workflow, performer result experience, external-source
integration, and Stash bridge that make this convenience plugin possible.

Please visit and support the original project:

- [Visage in Stash CommunityScripts](https://github.com/stashapp/CommunityScripts/tree/main/plugins/visage)
- [Original Visage repository](https://github.com/cc1234475/visage)
- [Visage discussion on the Stash forum](https://discourse.stashapp.cc/t/visage/11785)
- [Support CC1234's work on Patreon](https://www.patreon.com/cw/cc12340)

This companion is independent, is not endorsed by the Visage creator, and
contains no Visage source code.

## What it does

Right-click a performer result card in the Visage modal. The plugin reads the
card's external stash-box performer ID, runs a read-only GraphQL lookup against
your local Stash, and shows an action to open the matching local performer
profile in a new browser tab.

If the performer is not present locally, the menu says **Not found in local
Stash** and offers the exact external profile link already supplied by Visage
(for example StashDB, JavStash, FansDB, or ThePornDB). If more than one local
record has the same external ID, each local match is shown separately.

## Install with Stash Plugin Manager

After this contribution is merged, open **Settings > Plugins > Available
Plugins**, use the default **Community (stable)** source, find **Visage Stash
Link**, and install it.

Until then, the maintainer's source can be added manually:

```text
https://raw.githubusercontent.com/MrX-Builds/Visage-Stash-Link/main/index.yml
```

## Manual installation

1. Download `VisageStashLink_v1.1.0.zip` from the
   [v1.1.0 release](https://github.com/MrX-Builds/Visage-Stash-Link/releases/tag/v1.1.0).
2. Extract the ZIP and copy the enclosed `VisageStashLink` folder into the
   Stash plugins directory.
3. In Stash, open **Settings > Plugins** and click **Reload plugins**.
4. Reload the Stash browser page once.

## Use

Open a Visage result modal and right-click a performer card. After the read-only
lookup completes, choose **Open [name] in local Stash**. When no local match
exists, choose **Open performer on [external source]** instead.

## Compatibility and scope

- Human-tested with Visage 2.10.0. Visage 2.10.1 changes only scene-list menu placement and leaves this performer-card path unchanged.
- Uses the same `FindPerformersDocument` and `stash_id_endpoint` lookup pattern
  used by Visage itself.
- Does not alter Visage files or intercept normal left-click selection.
- Performs no GraphQL mutations and makes no Stash metadata changes.



## LLM-assisted development disclosure

Version 1.1.0 was developed with LLM assistance. The maintainer reviewed the
resulting plugin, human-tested both the local-Stash and external-profile paths
in a live Stash installation, and accepts responsibility for the code and
license compliance.

## License

MIT. See [LICENSE.md](LICENSE.md).
