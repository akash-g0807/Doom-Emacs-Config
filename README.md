# DOOM EMACS CONFIG MACOS

# IMAGES

## Install Brew

``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Literate Config
Found in: [config.org](./config.org)

# Install Emacs
On Mac-OS I use the [Emacs-plus](https://github.com/d12frosted/homebrew-emacs-plus) distribution.

``` bash
brew tap d12frosted/emacs-plus
brew install emacs-plus@29 --with-ctags --with-poll --with-debug --with-dbus --with-modern-pen-lds56-icon --with-native-comp --with-mailutils --with-imagemagick
```

## Pre-requisites

- **Fonts**

You can download the JetBrains font here: [JetBrains Mono Font](https://www.jetbrains.com/lp/mono/)

Install the Ubuntu fonts from here: [Ubuntu Fonts](https://design.ubuntu.com/font)
> [!NOTE]
> The variable pitch font for `org-mode` files use Cantarall font. Should be installed by default on distros like Ubuntu and Pop!_OS. If not, please download and install this font as well.

- **Install XCode tools**

``` bash
xcode-select --install
```

- **Install lldb**

``` bash
lldb
```
This will prompt and install. Do the same for `git`

- **Install `cmake`**

Needed to compile vterm

``` bash
brew install cmake
```

- **Install pip**

``` bash
python3 -m ensurepip
```

- **Install Pyright LSP Server**

``` bash
brew install pyright
```

- **C-Library to increase magit speed**

``` bash
brew install libgit2
```

- **GNU file, shell and text utilities**

``` bash
brew install coreutils
```

- **Install MacTex**

``` bash
brew install mactex
```

- **CCLS**

``` bash
brew install ccls
```

- **Install Rust and `rust-analyzer`**

Install rust by following the official website: [Install Rust](https://www.rust-lang.org/tools/install)

And now install `rust-analyzer`

``` bash
rustup componet add rust-analyzer
```

If you want to update components added from `rustup`, run:

``` bash
rustup update
```

- **Install `texlab` LSP Server**

Installation instructions: [texlab GitHub](https://github.com/latex-lsp/texlab)

- **Install GDB**

`gdb` is used for Rust and C/C++ debugging.

``` bash
brew install gdb
```

 - **Install `graphviz`**

This is needed for `org-roam` to generate graph visualisations.

``` bash
brew install graphviz
```

- **Install `ripgrep`**

``` bash
brew install ripgrep
```

- **Install X11 Clipboard**

``` bash
brew install xclip
```

- **Install glslang-tools**

``` bash
brew install glslang
```

- **Install libtool**

``` bash
brew install libtool
```

- **Install aspell**

``` bash
brew install aspell
```

- **Install fd**

``` bash
brew install fd
```

- **imagemagick**

``` bash
brew install imagemagick
```

- **dvisvgm and macsvg**

``` bash
brew install --cask macsvg
```

dvisvgm and dvipg hould be installed by default but if not run the following command after installing mactex

``` bash
sudo tlmgr update --self 
sudo /Library/TeX/texbin/tlmgr install dvisvgm
sudo /Library/TeX/texbin/tlmgr install dvipng
```

Or build from source: [Script download here](https://gist.github.com/tobywf/aeeeee63053aaaa841b4032963406684)

- **Install pyenv**

``` bash
brew install pyenv
```

- **Install pipvenv**

``` bash
brew install pipvenv
```

- **Install pytest**

``` bash
brew install pytest
```

- **Install cpptest**

``` bash
brew install cpptest
```


- **Install png paste**

Needed to make org-download work

``` bash
brew install pngpaste
```


## Installation

1. First install Emacs. Latest version is recommended. Use the instructions above
2. Install Doom Emacs:

``` bash
git clone --depth 1 https://github.com/doomemacs/doomemacs ~/.config/emacs
~/.config/emacs/bin/doom install
```
More details about Doom Emacs can be found in the GitHub page: [Doom Emacs GitHub](https://github.com/doomemacs/doomemacs)

Run `doom sync` after installing Doom Emacs.
Rm `doom env` after installing Doom Emacs

3. Download the repo and copy the contents of this repo to the directory: `~/.config/doom`
4. Run `doom sync` command after copying the contents.
5. Create a folder `+STORE` in your home directory
6. Add `export PATH="$HOME/.config/emacs/bin/:$PATH"` to your `~/.zshrc` or `~/.bashrc`
7. Run `doom doctor` and install any software you need/want to

## Post Install

- In Emacs, run:
  - `M-x all-the-icons-install-fonts`
  - `M-x nerd-icons-install-fonts`
  - `M-x dap-cpp-tools-setup`
  - `M-x dap-codelldb-setup`

- `M-x treesit-install-language-grammar`
- `M-x customize-group` and change elcord to use `ts-mode` to have the correct Discord rich presence icon.
## TODO
- Update README Images
- GitHub Copilot
