# NixOS SD image for VisionFive 2 boards

Using https://github.com/NixOS/nixos-hardware/pull/608

The `flake.nix` here is taken from the `starfive/visionfive/v2/README.md`
file in that PR.

Building the SD image requires at least 31 GiB under `/tmp`. I had to set
`boot.tmpOnTmpfs` to `false` in my NixOS host to be able to build it,
because the 16 GiB of RAM it got were not enough.
