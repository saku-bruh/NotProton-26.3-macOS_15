# NotProton

NotProton is a community macOS tool for enabling Steam Play through CrossOver and porting the
Wine/Proton components needed by Windows games.

This fork adds experimental support for **CrossOver 26.3.0.39832** on Apple Silicon using Rosetta.
It is not affiliated with Valve or CodeWeavers.

[Download NotProton 1.0.3 for CrossOver 26.3](https://github.com/burhanmoin1/NotProton-crossover-26.3/releases/download/v1.0.3/NotProton-1.0.3.dmg)

## Compatibility

- Steam Client 1788652215 or 1790121765.
- CrossOver 26.3.0.39832, Rosetta runner.
- This CrossOver bundle does not include the aarch64 Windows runtime needed for FEX.
- Steam game launch has not yet been smoke-tested on this fork.
- CrossOver Preview builds 20260821 and 20261006 have separate pins; the default bridge build targets stable 26.3.

NotProton enables Steam Play functionality already present but inactive in the macOS Steam client,
and ports selected components of Valve's Proton to macOS.

The macOS app itself is located in the ```app``` folder. The core logic is in ```dylib```.
```lsteamclient``` is a macOS port of Valve's lsteamclient. ```steam-shim```is a port of Valve's
steam-helper from Proton 9. ntdll-patch patches the copy of CrossOver that the app
makes/places in the ```~/Library/Application Support/notproton/runners/``` folder so that
lsteamclient is loaded.

Please read NOTICE for license information.

Please open issue reports with any issues. PRs are welcome and encouraged. Contributions policy to come shortly.
