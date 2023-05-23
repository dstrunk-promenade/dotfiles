# Dotfiles

There are many like them, but these are mine.

## Setting up a new computer

New computer is pretty straightforward. Using iCloud Desktop, things are even simplier: sharing files from one computer to another, such as PGP keys or TablePlus connections, entails moving files from your old computer onto the iCloud Desktop for immediate retrieval on the new computer. For everything else, Homebrew + git + Google synced profiles handles everything.

1. Install Homebrew
1. Download this repository (`git` will not be installed yet; it gets installed as part of the next step)
1. Run `brew bundle`
1. symlink `.git*` files to the home directory (`~`)
1. `ssh-keygen -t ed25519 -C {your-email@example.com}`, import this into GitHub
1. Export PGP key from previous computer, import into new computer. For information on this step, see <https://www.phildev.net/pgp/gpg_moving_keys.html>.
1. Export TablePlus connections from previous computer, import into new computer.

## Manual steps

1. Mac login
1. Google Chrome sync - requires logging into Google account
1. PhpStorm sync - requires logging into JetBrains account
1. Bartender - requires manual addition of license, manual configuration of settings
1. TablePlus - requires manual addition of license, importing connections from old computer
1. OmniFocus - requires logging into Omni account
1. Obsidian - fully manual set up. Requires the following:
    1. Using iCloud, set up folder where Obsidian notes exist (typically `iCloud Drive/Obsidian`)
    1. Turn on Vim mode
    1. Enable community plugins
    1. Install `Templater`

## Troubleshooting
### `gpg: signing failed: Inappropriate ioctl for device`

Run `export GPG_TTY=$(tty)`
