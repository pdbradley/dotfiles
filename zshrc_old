# had to preload compdef https://github.com/memborsky/dotfiles/commit/0cd2e69463d25bb0d9fa17710c7a8ed8f54a018f
autoload -U compinit compdef
compinit

# complete g like git
compdef g=git

function g {
   if [[ $# > 0 ]]; then
     git $@
   else
     git status
   fi
}

transfer() { if [ $# -eq 0 ]; then echo "No arguments specified. Usage:\necho transfer /tmp/test.md\ncat /tmp/test.md | transfer test.md"; return 1; fi 
  tmpfile=$( mktemp -t transferXXX ); if tty -s; then basefile=$(basename "$1" | sed -e 's/[^a-zA-Z0-9._-]/-/g'); curl --progress-bar --upload-file "$1" "https://transfer.sh/$basefile" >> $tmpfile; else curl --progress-bar --upload-file "-" "https://transfer.sh/$1" >> $tmpfile ; fi; cat $tmpfile; rm -f $tmpfile; } 


export VISUAL=nvim
export PATH="/Users/philip/dotfiles/bin:$PATH"

### Added by the Heroku Toolbelt
export PATH="/usr/local/heroku/bin:$PATH"
export PATH="/usr/local/mysql/bin:$PATH"
export PATH="/Applications/Postgres.app/Contents/Versions/latest/bin:$PATH"

#flutter path
export PATH="/Users/philip/flutter/bin:$PATH"

export PKG_CONFIG_PATH="/usr/local/opt/pkg-config:$PKG_CONFIG_PATH"

export EDITOR='nvim'

export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES

autoload -Uz compinit && compinit

export PATH="$HOME/bin:$PATH"
export PATH="$HOME/bin/jruby-9.1.2.0/bin:$PATH"


# for erlang / iex
export ERL_AFLAGS="-kernel shell_history enabled"

source $HOME/dotfiles/zsh/prompt
source $HOME/dotfiles/zsh/aliases

# added by travis gem
[ -f /Users/philip/.travis/travis.sh ] && source /Users/philip/.travis/travis.sh

# autojump
[ -f /usr/local/etc/profile.d/autojump.sh ] && . /usr/local/etc/profile.d/autojump.sh

#source ~/bin/tmuxinator.zsh

bindkey "^P" up-line-or-search
bindkey "^A" vi-beginning-of-line

. $HOME/.asdf/asdf.sh

#. $HOME/.asdf/completions/asdf.bash

#export PATH="$(brew --prefix qt@5.5)/bin:$PATH"

# twilio autocomplete setup
TWILIO_AC_ZSH_SETUP_PATH=/Users/philip/.twilio-cli/autocomplete/zsh_setup && test -f $TWILIO_AC_ZSH_SETUP_PATH && source $TWILIO_AC_ZSH_SETUP_PATH;

export PATH="$PATH:`yarn global bin`"

export PATH="/usr/local/opt/node@10/bin:$PATH"

# Added by serverless binary installer
export PATH="$HOME/.serverless/bin:$PATH"

# The next line updates PATH for Netlify's Git Credential Helper.
if [ -f '/Users/philip/.netlify/helper/path.zsh.inc' ]; then source '/Users/philip/.netlify/helper/path.zsh.inc'; fi

export PATH="$HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH"


[ -f ~/.fzf.zsh ] && source ~/.fzf.zsh
