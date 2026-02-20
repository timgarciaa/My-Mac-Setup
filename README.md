# My-Mac-Setup

1. Install Brew
2. Install Git
3. Install iTerm
4. Install zsh `sudo apt install zsh`
5. Install OhMyZsh `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
6. Install PowerLevel10k `git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k`
7. Configure theme to 'powerlevel10k/powerlevel10k' `vim ~/.zshrc`
8. `source ~/.zshrc`
9. Add zsh-autosuggestions `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
10. Add zsh-syntax-highlighting `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
11. Add them to plugins `plugins=(git zsh-autosuggestions zsh-syntax-highlighting)`
12. Install NVM and node follow node.js guide using nvm with pnpm.
14. Install VSCode
15. Install GH `brew install gh`
16. Setup git config name `git config --global user.name "{name}"`
17. Setup git config email `git config --global user.email "{email}"`
18. Install tmux `brew install tmux`
19. Create folder `mkdir -p ~/.tmux/plugins`
20. Install tpm `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
21. Update tmux config at `~/.config/tmux/tmux.conf`:
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
19. Install plugins ```cd ~/.tmux/plugins/tpm/scripts && ./install_plugins.sh``` OR start a new tmux session and do Ctrl + Space followed by Capital I.
20. Install nvim
