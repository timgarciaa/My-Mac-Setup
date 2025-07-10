# My-Mac-Setup

1. Install Brew
2. Install Git
3. Install iTerm
4. Install zsh `sudo apt install zsh`
5. Install OhMyZsh `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
6. Install PowerLevel10k `git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k`
7. Configure theme to 'powerlevel10k/powerlevel10k' `vim ~/.zshrc`
8. Source `vim ~/.zshrc`
9. Add zsh-autosuggestions `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
10. Add zsh-syntax-highlighting `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
11. Install NVM
12. Install Node
13. Install VSCode
14. Install GH
15. Setup git config name `git config --global user.name "{name}"`
16. Setup git config email `git config --global user.email "{email}"`


17. Install tmux
18. Install tpm
Tmux config:

```
set-option -sa terminal-overrides ",xterm*:Tc"

unbind C-b
set -g prefix C-Space
bind C-Space send-prefix

bind -n M-H previous-window
bind -n M-L next-window

set -g base-index 1
set -g pane-base-index 1
set-window-option -g pane-base-index 1
set-option -g renumber-windows on

set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'christoomey/vim-tmux-navigator'
set -g @plugin 'catppuccin/tmux'

run '~/.tmux/plugins/tpm/tpm'
```
