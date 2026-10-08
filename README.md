# NotProton

NotProton enables the Steam Play experience from Linux Steam in the macOS Steam client.

This is done by forcibly enabling the Steam Play functionality in macOS Steam (which is
present and inert) as well as by porting some components of Valve's Proton to macOS.

The supported stable setup is Steam Client 1788652215 or 1790121765 with **CrossOver 26.3.0.39832**.
This CrossOver bundle supports the Rosetta runner; it does not include the aarch64 Windows runtime
needed for FEX. CrossOver Preview builds 20260821 and 20261006 have separate pins. The default
bridge build targets the stable 26.3 runtime.

The macOS app itself is located in the ```app``` folder. The core logic is in ```dylib```.
```lsteamclient``` is a macOS port of Valve's lsteamclient. ```steam-shim```is a port of Valve's
steam-helper from Proton 9. ntdll-patch patches the copy of CrossOver that the app
makes/places in the ```~/Library/Application Support/notproton/runners/``` folder so that
lsteamclient is loaded.

This release is coming several days past when I wanted to release it, so the
documentation is quite sparse. Sorry about that, I'll improve it shortly.

Please read NOTICE for license information.

Please open issue reports with any issues. PRs are welcome and encouraged. Contributions policy to come shortly.
