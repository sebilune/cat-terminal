## Installation
This theme relies on starship for its functionality. Therefore, you will need to install starship on your system. The first two steps are snippets from the official [starship docs](https://starship.rs/guide/) to help you get started. =^..^=

### Step 1. Install Starship

Select your operating system from the list below to view installation instructions:

<details>
<summary>Android</summary>

Install Starship using any of the following package managers:

| Repository | Instructions           |
| ---------- | ---------------------- |
| [Termux]   | `pkg install starship` |

</details>

<details>
<summary>BSD</summary>

Install Starship using any of the following package managers:

| Distribution | Repository      | Instructions                      |
| ------------ | --------------- | --------------------------------- |
| **_Any_**    | **[crates.io]** | `cargo install starship --locked` |
| FreeBSD      | [FreshPorts]    | `pkg install starship`            |
| NetBSD       | [pkgsrc]        | `pkgin install starship`          |

</details>

<details>
<summary>Linux</summary>

Install the latest version for your system:

```sh
curl -sS https://starship.rs/install.sh | sh
```

Alternatively, install Starship using any of the following package managers:

| Distribution       | Repository              | Instructions                                                  |
| ------------------ | ----------------------- | ------------------------------------------------------------- |
| **_Any_**          | **[crates.io]**         | `cargo install starship --locked`                             |
| _Any_              | [conda-forge]           | `conda install -c conda-forge starship`                       |
| _Any_              | [Linuxbrew]             | `brew install starship`                                       |
| Alpine Linux 3.13+ | [Alpine Linux Packages] | `apk add starship`                                            |
| Arch Linux         | [Arch Linux Extra]      | `pacman -S starship`                                          |
| CentOS 7+          | [Copr]                  | `dnf copr enable atim/starship` <br /> `dnf install starship` |
| Gentoo             | [Gentoo Packages]       | `emerge app-shells/starship`                                  |
| Manjaro            |                         | `pacman -S starship`                                          |
| NixOS              | [nixpkgs]               | `nix-env -iA nixpkgs.starship`                                |
| openSUSE           | [OSS]                   | `zypper in starship`                                          |
| Void Linux         | [Void Linux Packages]   | `xbps-install -S starship`                                    |

</details>

<details>
<summary>macOS</summary>

Install the latest version for your system:

```sh
curl -sS https://starship.rs/install.sh | sh
```

Alternatively, install Starship using any of the following package managers:

| Repository      | Instructions                            |
| --------------- | --------------------------------------- |
| **[crates.io]** | `cargo install starship --locked`       |
| [conda-forge]   | `conda install -c conda-forge starship` |
| [Homebrew]      | `brew install starship`                 |
| [MacPorts]      | `port install starship`                 |

</details>

<details>
<summary>Windows</summary>

Install the latest version for your system with the MSI-installers from the [releases section](https://github.com/starship/starship/releases/latest).

Install Starship using any of the following package managers:

| Repository      | Instructions                            |
| --------------- | --------------------------------------- |
| **[crates.io]** | `cargo install starship --locked`       |
| [Chocolatey]    | `choco install starship`                |
| [conda-forge]   | `conda install -c conda-forge starship` |
| [Scoop]         | `scoop install starship`                |
| [winget]        | `winget install --id Starship.Starship` |

</details>

### Step 2. Set up your shell to use Starship

Configure your shell to initialize starship. Select yours from the list below:

<details>
<summary>Bash</summary>

Add the following to the end of `~/.bashrc`:

```sh
eval "$(starship init bash)"
```

</details>

<details>
<summary>Cmd</summary>

You need to use [Clink](https://chrisant996.github.io/clink/clink.html) (v1.2.30+) with Cmd.
Create a file at this path `%LocalAppData%\clink\starship.lua` with the following contents:

```lua
load(io.popen('starship init cmd'):read("*a"))()
```

</details>

<details>
<summary>Elvish</summary>

Add the following to the end of `~/.elvish/rc.elv`:

```sh
eval (starship init elvish)
```

Note: Only Elvish v0.18+ is supported

</details>

<details>
<summary>Fish</summary>

Add the following to the end of `~/.config/fish/config.fish`:

```fish
starship init fish | source
```

</details>

<details>
<summary>Ion</summary>

Add the following to the end of `~/.config/ion/initrc`:

```sh
eval $(starship init ion)
```

</details>

<details>
<summary>Nushell</summary>

Add the following to the end of your Nushell env file (find it by running `$nu.env-path` in Nushell):

```sh
mkdir ~/.cache/starship
starship init nu | save -f ~/.cache/starship/init.nu
```

And add the following to the end of your Nushell configuration (find it by running `$nu.config-path`):

```sh
use ~/.cache/starship/init.nu
```

Note: Only Nushell v0.78+ is supported

</details>

<details>
<summary>PowerShell</summary>

Add the following to the end of your PowerShell configuration (find it by running `$PROFILE`):

```powershell
Invoke-Expression (&starship init powershell)
```

</details>

<details>
<summary>Tcsh</summary>

Add the following to the end of `~/.tcshrc`:

```sh
eval `starship init tcsh`
```

</details>

<details>
<summary>Xonsh</summary>

Add the following to the end of `~/.xonshrc`:

```python
execx($(starship init xonsh))
```

</details>

<details>
<summary>Zsh</summary>

Add the following to the end of `~/.zshrc`:

```sh
eval "$(starship init zsh)"
```

</details>

### Step 3: Bring the kitty to life

Clone this repository containing the theme file (`starship.toml`) using the following command, assuming you have git installed:

```bash
git clone https://github.com/sebiram/cat-terminal.git ~/.config/
```