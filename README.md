# urxvt_tmux

My urxvt+tmux configuration

design goals:  
* smoothly working on WSL and Linux    
* **Control+Shift** as leader keys for URxvt
* **\`** as leader key for tmux
* avoiding conflicts with default keybindings of **emacs** and **vim** 
* extented mouse support
* effective usage on the Lenovo ThinkPad keyboards  

urxvt:  
* all plugins are declared via **URxvt.perl-ext-common:**  
* some plugins may be changed and will be stored directly in this repository, into: `./.urxvt/ext`  

tmux:  
* tmux plugins can be easily find in the github (are declared via **set -g @tpm_plugins ''**)  

dependencies:  
* FantasqueSansMono font : https://github.com/belluzj/fantasque-sans
* xsel  
* xclip  
* OPTIONAL: add in your **~/.zshrc** or **~/.bashrc** :
```
if [[ $TERM == 'rxvt-unicode-256color' && -z "$TMUX" ]]; then exec tmux -f $HOME/.tmux/tmux.conf; fi
```
https://unix.stackexchange.com/questions/43601/how-can-i-set-my-default-shell-to-start-up-tmux
