# Enabling Speaker Audio on 15" Razer Blade 2023 

Basic enablement patch from blindly applying settings obtained here: https://bugzilla.kernel.org/show_bug.cgi?id=207423

## Requires

`alsa-tools`

## tested on
- Razer Blade 15 2023 model - RZ09-0485Z
- Ubuntu 24.04

## Execution

To manually bring up sound on this machine execute this script with root privileges.

## Systemd Service

Alternatively you can set this to automatically apply at boot by using the systemd service

1. Copy the script to `/opt/bin/` as root 
2. Copy the service file to `/etc/systemd/system/` as root
3. Run `systemctl daemon-reload` to pick up the new daemon
4. enable at login with `sudo systemctl enable razer_blade_2023_sound.service`
