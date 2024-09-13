<p align="center">
  <a href="https://github.com/mingyuchoo/doom-emacs-configurations/blob/main/LICENSE"><img alt="license" src="https://img.shields.io/github/license/mingyuchoo/doom-emacs-configurations"/></a>
  <a href="https://github.com/mingyuchoo/doom-emacs-setting/issues"><img alt="Issues" src="https://img.shields.io/github/issues/mingyuchoo/doom-emacs-setting?color=appveyor" /></a>
  <a href="https://github.com/mingyuchoo/doom-emacs-setting/pulls"><img alt="GitHub pull requests" src="https://img.shields.io/github/issues-pr/mingyuchoo/doom-emacs-setting?color=appveyor" /></a>
</p>

# doom-emacs-setting

## Install Doom Emacs on macOS

Install Emacs first

```bash
brew install emacs
brew install coreutils
brew install grep
brew install pandoc
brew install rlwrap # for SBCL REPL
```

Install Doomemacs and sync it

```bash
git clone --depth 1 --single-branch https://github.com/doomemacs/doomemacs ~/.config/emacs
$HOME/.config/emacs/bin/doom install
$HOME/.config/emacs/bin/doom sync
$HOME/.config/emacs/bin/doom doctor
```

## Add `$HOME/.emacs.d/bin` to `$PATH`

```bash
...
export $PATH="$HOME/.config/emacs/bin:$PATH"
```


## Install fonts

Run emacs, and do this to install fonts

`M-x nerd-icons-install-fonts``


## Improve startup time

To start the server run on Arch Linux

```bash
# emacs --daemon
systemctl --user enable --now emacs
```

And then to start a client run

```bash
emacsclient -nw -c
```

Other solutions in `.bashrc`

```bash
# environment
export EDITOR='emacsclient -t'
export VISUAL='emacsclient -t'

# aliases
alias emacs="emacsclient -nw -c -a 'emacs'"
```

## Reference

-<https://github.com/hlissner/doom-emacs>
-<https://github.com/hlissner/doom-emacs/blob/master/docs/getting_started.org>
-<https://gist.github.com/ecthiender/b9db474e80113bdc18d472de1593eb3c>
