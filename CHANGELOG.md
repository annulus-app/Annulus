# Changelog

Notable changes to Annulus, newest first. Versions follow [Semantic Versioning](https://semver.org). Until 1.0, a minor version may change the vault or the sync protocol, and its notes will say how to move across.

## 0.2.0 (2026-11-17)

### Terminal and SSH

- Open and switch between local terminal tabs while the vault is locked. The plus button opens your default local shell, and vault-backed tabs stay hidden until you unlock.
- Selecting a terminal tab puts keyboard focus back in its last active pane so you can type right away.
- SSH tabs close on a clean exit and select the next session. You can turn this off in Settings under Sessions. Dropped connections still follow their reconnect settings.

### Agent access

- An agent can request `sudo` in its SSH tab through `annulus-agent elevate` or the `annulus_elevate` MCP tool. Annulus asks you for the SSH password and sends it directly to `sudo`. The agent never receives it.

### Windows downloads

- The Windows x64 installer, portable client, and separate sync server are available for this release. The binaries are unsigned.

## 0.1.0 (2026-11-11)

The first public version. This release has the Windows downloads; the macOS and Linux ones follow. Builds aren't signed yet.

### In the app

- Local terminals, with PowerShell, cmd, WSL, Git Bash and login shells found for you.
- SSH with passwords and keys, jump host chains, SOCKS5 and HTTP proxies, `ProxyCommand` and automatic reconnects. A changed server key stops the connection.
- Hosts in nested groups that pass their settings down, with tags, search and quick connect. Import from `ssh_config` and `known_hosts`.
- A keychain that generates and imports Ed25519, ECDSA and RSA keys, and installs them on servers or takes them off again.
- SFTP in two panes, with a transfer queue that picks up where it left off and a choice of what happens to files that already exist.
- Local, remote and SOCKS port forwarding, with a wizard that draws each kind.
- Split panes, broadcast input and focus mode.
- Full-screen programs such as btop, htop and vim get the mouse when they ask for it (clicks, drags and the wheel; Shift still selects text), and braille graphs, block meters and symbols from fallback fonts stay on the terminal's grid.
- Snippets, encrypted session logs, a command palette, editable shortcuts and 498 color schemes.
- An encrypted vault that auto-locks, and a recovery key.
- A local control door for scripts and coding agents, off until you switch it on.

### The sync server

- A single binary or Docker image, with several separate accounts and closed sign-ups by default.
- End-to-end encrypted sync with OPAQUE login, earlier versions kept on the server, a 30-day trash and a device list.
- Built-in TLS, or a certificate of its own that devices trust by fingerprint.

### On the way

FIDO2 and hardware-backed keys, SSH certificates, keyboard-interactive login, saved workspaces, autocomplete, installers, signing and update checks.
