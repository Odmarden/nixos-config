# NixOS System Configuration

NixOS system configuration files, symlinked from `/etc/nixos/`.

> [!NOTE]
> `hardware-configuration.nix` is hardware-specific (generated per-machine by `nixos-generate-config`) and is excluded from this repository.

## Structure

- `configuration.nix`: Main system configuration (networking, locale, GDM, packages, PipeWire, users). Imports `/etc/nixos/hardware-configuration.nix` locally.
- `hyprland.nix`: System module enabling Hyprland Wayland compositor, XDG portals, and desktop essentials.
- `gdm-background.jpg`: Custom background applied to the GDM login screen.

## Setup / Symlinks

To link this repository to `/etc/nixos/`:

```bash
sudo ln -sfn $(pwd)/configuration.nix /etc/nixos/configuration.nix
sudo ln -sfn $(pwd)/hyprland.nix /etc/nixos/hyprland.nix
```

To rebuild and apply changes:

```bash
sudo nixos-rebuild switch
```
