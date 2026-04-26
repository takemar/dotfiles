# dotfiles

https://www.chezmoi.io/

## Prerequisite

### Install chezmoi

https://www.chezmoi.io/install/

- On Arch Linux: `sudo pacman -S chezmoi`
- On Windows: `winget install twpayne.chezmoi`

### Install Bitwarden CLI

https://bitwarden.com/help/cli/

(Optional; for SSH keys)

- On Arch Linux: `sudo pacman -S bitwarden-cli`
- On Windows
    1. Download from the official page
    1. Copy the binary to `C:\Program Files\bw`
    1. Add the directory to PATH

Then

1. `bw config server "https://bitwarden.example"`
1. `bw login`

### Install wsl2-ssh-agent

(Optional; for SSH keys on WSL)

https://github.com/mame/wsl2-ssh-agent

1. Install by following the insturction on GitHub README 
    - AUR package is also available
1. Copy the [`wsl2-ssh-agent.service`](https://github.com/mame/wsl2-ssh-agent/blob/main/extras/systemd/user/wsl2-ssh-agent.service) file to `/usr/lib/systemd/user`
    - Note that this file is not included in the AUR package for now
1. `systemctl --user enable --now wsl2-ssh-agent.service`

## Initial Setup

1. `chezmoi init takemar`
1. `chezmoi edit-config`
1. `chezmoi apply`
