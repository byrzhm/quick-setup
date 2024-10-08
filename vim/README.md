## Install neovim

### Build from source

Install dependencies

```sh
sudo apt-get install -y ninja-build gettext
### sudo apt-get install ninja-build gettext cmake unzip curl build-essential

git clone git@github.com:neovim/neovim
cd neovim && make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install
```

### Use pre-built

```sh
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz
sudo rm -rf /opt/nvim
sudo tar -C /opt -xzf nvim-linux64.tar.gz
```

Then add this to your shell config (~/.bashrc, ~/.zshrc, ...):

```sh
export PATH="$PATH:/opt/nvim-linux64/bin"
```

## Use LazyVim

See [https://www.lazyvim.org/installation](https://www.lazyvim.org/installation).

```sh
# required
mv ~/.config/nvim{,.bak}

# optional but recommended
mv ~/.local/share/nvim{,.bak}
mv ~/.local/state/nvim{,.bak}
mv ~/.cache/nvim{,.bak}

git clone git@github.com:LazyVim/starter ~/.config/nvim
rm -rf ~/.config/nvim/.git
```

