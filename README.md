# Tools for configuring [notWG](https://github.com/el3xyz/wireguard-linux-compat).

WARNING: notWG protocol is incompatible with WireGuard but both types of devices can co-exist on the same host.

## Building

    $ cd src
    $ make DEV=<name>

Where `<name>` is the type of network device chosen during [driver](https://github.com/el3xyz/wireguard-linux-compat) compilation.

## Installing
    # Sandbox installation is required to avoid conflicts between system WG tools and ours.
    $ make DEV=<name> PREFIX=<sandbox_dir> WITH_SYSTEMDUNITS=no install

Where `<name>` should match the name provided during driver and tools compilation.
Use <sandbox_dir>/bin/wg-quick and <sandbox_dir>/bin/wg for configuring obfuscated tunnel. 

## License

This project is released under the [GPLv2](COPYING).
