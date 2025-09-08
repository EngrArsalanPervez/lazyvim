# Installations


## Pre-Requisites

```bash
sudo apt install xclip ripgrep curl universal-ctags git build-essential cmake python3-venv python3-dev python3-pip ack fd-find clang-format -y 
sudo apt install python3-pynvim -y
sudo ln -s /usr/bin/fdfind /usr/bin/fd
fd

sudo apt install tmux fish luarocks
```

## Lazygit

```bash
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit /usr/local/bin
```

## Install neovim

```bash
wget https://github.com/neovim/neovim/releases/download/nightly/nvim.appimage --output-document nvim
chmod +x nvim
sudo chown root:root nvim
sudo mv nvim /usr/bin
mkdir -p ~/.config/nvim
sudo mkdir -p /root/.config/nvim
```

## Fonts

```bash
cd ~
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.1/ComicShannsMono.zip
unzip ComicShannsMono.zip
sudo cp Comic*.otf /usr/share/fonts/
sudo cp Comic*.otf /usr/local/share/fonts/
rm *.otf
rm ComicShannsMono.zip
```


## Lazyvim

```bash
# required
mv ~/.config/nvim{,.bak}

# optional but recommended
mv ~/.local/share/nvim{,.bak}
mv ~/.local/state/nvim{,.bak}
mv ~/.cache/nvim{,.bak}


git clone https://github.com/LazyVim/starter ~/.config/nvim
rm -rf ~/.config/nvim/.git
nvim


:LazyHealth
```


## Plugins

```bash
l
x
:Mason
```

## multicursor.lua
```bash
nano ~/.config/nvim/lua/plugins/multicursor.lua
return {
  "mg979/vim-visual-multi",
  branch = "master",
  lazy = false, -- load immediately
}
```

## Source

Project Implemented on [Academic Master](https://academic-master.com/)
