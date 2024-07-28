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

## Improve startup time

To start the server run

```bash
emacs --daemon
```

And then to start a client run

```bash
emacsclient -nw -c
```

Other solutions in `.bashrc`

```bash
alias de="emacsclient -t -a \"\""
```

## Reference

-<https://github.com/hlissner/doom-emacs>

-<https://github.com/hlissner/doom-emacs/blob/master/docs/getting_started.org>

-<https://gist.github.com/ecthiender/b9db474e80113bdc18d472de1593eb3c>
