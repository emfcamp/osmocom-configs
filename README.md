# osmocom experiments

You need:

- osmoBSC (`osmo-bsc.cfg`, `nix-shell -p osmobsc`)
- osmoHLR (`osmo-hlr.cfg`, `nix-shell -p osmohlr`)
- 2x osmoMGW (`osmo-mgw-*.cfg`, run one for each config file, `nix-shell -p osmomgw`)
- osmoMSC (`osmo-msc.cfg`, `nix-shell -p osmomsc`)
- osmoSTP (`osmo-stp.cfg`, `nix-shell -p libosmo-sccp`)

I used Nix to get all of the binaries (see the nix-shell invocations), but you can also get them from the osmocom
website or perhaps your local distro if you're lucky. (You can get nix [here](https://nixos.org/download/) with a curl-pipe-bash
thingie.)

You also need a BTS pointed at osmoBSC -- edit `osmo-bsc.cfg` to configure what it is and the settings for it. (It's currently
configured for a sysmoBTS in the Ofcom shared access band.)

The [osmocom wiki](https://osmocom.org/projects/cellular-infrastructure/wiki/Osmocom_Network_In_The_Box) has more docs and is
generally helpful -- you'll want to download the PDF manuals for the thing you're trying to configure.

