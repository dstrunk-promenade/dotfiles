# Dotfiles

There are many like them, but these are mine.

## Setting up a new computer

1. Install Homebrew
1. Download this repository (`git` will not be installed yet; it gets installed as part of the next step)
1. Run `brew bundle`
1. symlink `.git*` files to the home directory (`~`)
1. `ssh-keygen -t ed25519 -C {your-email@example.com}`, import this into GitHub
1. Export PGP key from previous computer, import into new computer. For information on this step, see <https://www.phildev.net/pgp/gpg_moving_keys.html>.

## Troubleshooting
### `gpg: signing failed: Inappropriate ioctl for device`

Run `export GPG_TTY=$(tty)`
