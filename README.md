## Installation

### Install Neovim
['stable'](https://github.com/neovim/neovim/releases/tag/stable)
['nightly'](https://github.com/neovim/neovim/releases/tag/nightly)


#### Nerd Font

['Roboto Mono Nerd Font'](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.3.0/RobotoMono.zip)

#### Windows Installation

<details>

1. install [chocolatey](https://chocolatey.org/install)
run in cmd as **admin**
```
winget install --accept-source-agreements chocolatey.chocolatey
```

2. install all requirements using choco, exit the previous cmd and
open a new one so that choco path is set, and run in cmd as **admin**:
```
choco install -y neovim git ripgrep wget fd unzip gzip mingw make
```

3.If you're using `cmd.exe`:

```
git clone https://github.com/kevin-wbt/kickstart.nvim.git "%localappdata%\nvim"
```
</details>

#### Fedora Install

<details>

1 install dependencies
```
sudo dnf install -y gcc make git ripgrep fd-find unzip neovim
```

2 clone repo

```sh
git clone https://github.com/kevin-wbt/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```

</details>

### multiple configs
<details>
  
   You can use [NVIM_APPNAME](https://neovim.io/doc/user/starting.html#%24NVIM_APPNAME)`=nvim-NAME`
    to maintain multiple configurations. For example, you can install the kickstart
    configuration in `~/.config/nvim-kickstart` and create an alias:
    ```
    alias nvim-kickstart='NVIM_APPNAME="nvim-kickstart" nvim'
    ```
    When you run Neovim using `nvim-kickstart` alias it will use the alternative
    config directory and the matching local directory
    `~/.local/share/nvim-kickstart`. You can apply this approach to any Neovim
    distribution that you would like to try out.
    
</details>

> **BACKUP**

<details>
  
| OS | PATH |
| :- | :--- |
| Linux, MacOS | `$XDG_CONFIG_HOME/nvim`, `~/.config/nvim` |
| Windows (cmd)| `%localappdata%\nvim\` |
| Windows (powershell)| `$env:LOCALAPPDATA\nvim\` |

</details>

