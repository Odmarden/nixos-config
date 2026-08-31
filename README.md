# NixOS System Configuration

NixOS system configuration files for my machine (`nixos`), symlinked from `/etc/nixos/`.

## Structure

- `configuration.nix`: Main system configuration (networking, locale, GDM, packages, PipeWire, users).
- `hardware-configuration.nix`: Auto-generated hardware and filesystem mappings.
- `hyprland.nix`: System module enabling Hyprland Wayland compositor, XDG portals, and desktop essentials.
- `gdm-background.jpg`: Custom background applied to the GDM login screen.

## Setup / Symlinks

To link this repository to `/etc/nixos/`:

```bash
sudo ln -sfn $(pwd)/configuration.nix /etc/nixos/configuration.nix
sudo ln -sfn $(pwd)/hardware-configuration.nix /etc/nixos/hardware-configuration.nix
sudo ln -sfn $(pwd)/hyprland.nix /etc/nixos/hyprland.nix
```

To rebuild and apply changes:

```bash
sudo nixos-rebuild switch
```
