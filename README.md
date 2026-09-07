# SDODS Scoop bucket

```powershell
scoop bucket add sdods https://github.com/siri1410/scoop-sdods
```

```powershell
scoop install sdods
```

Installs the **SDODS desktop app** — BDD test automation for UI, API and hybrid flows,
<https://sdods.com>. For the command line on Windows, use npm (`npm install -g @sdods/cli`) or the
PowerShell installer at <https://sdods.com/install>.

## The manifest arrives with the first desktop release

`bucket/` is empty until a `desktop-v*` release is published, and that is deliberate rather than
unfinished: the manifest carries the SHA-256 of the installer it downloads, so it cannot be written
before that installer exists. `scripts/sync-channels.ts` in the SDODS repository renders it from the
real release asset and never from a transcribed checksum.

Until then `scoop install sdods` will not find a manifest here. sdods.com does not advertise this
channel until it does.
