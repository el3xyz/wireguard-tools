# Tools for configuring [WireGuard](https://www.wireguard.com/) with obfuscation support (wiregurad_obf)

Obfuscated WireGurad protocol and device name is wireguard_obf. Protocol is incompatible with original WireGuard but both types of devices can co-exist on the same host.

## Building

    $ cd src
    $ make DEV=wireguard_obf

Sandbox installation is recommended to not intermix tools for obfuscated and original WireGuard.

## Installing

    # make DEV=wireguard_obf PREFIX=<sandbox_dir> WITH_SYSTEMDUNITS=no install

Use <sandbox_dir>/bin/wg-quick and <sandbox_dir>/bin/wg for configuring obfuscated tunnel. 

## License

This project is released under the [GPLv2](COPYING).
