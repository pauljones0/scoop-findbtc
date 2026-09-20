# scoop-findbtc

Scoop bucket for [findbtc](https://github.com/pauljones0/findbtc)
(scan raw block devices and forensic images for BTC wallet traces).

    scoop bucket add findbtc https://github.com/pauljones0/scoop-findbtc
    scoop install findbtc

Verify the install with a synthetic scan:

    $smoke = Join-Path $env:TEMP 'fbt-smoke.bin'
    Set-Content -NoNewline -Path $smoke -Value 'x wallet.dat y'
    findbtc $smoke

## Maintenance

`bucket/findbtc.json` pins an immutable release asset (URL +
SHA-256). The scheduled `checkver` workflow bumps it automatically
when findbtc releases (the manifest's `checkver`/`autoupdate`
stanzas drive that); review its commits like any other.
