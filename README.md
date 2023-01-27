# doom-emacs-setting

## Install Doom Emacs

```bash
git clone --depth 1 https://github.com/hlissner/doom-emacs ~/.emacs.d
$HOME/.emacs.d/bin/doom install
$HOME/.emacs.d/bin/doom sync
```

## Add `$HOME/.emacs.d/bin` to `$PATH`

```bash
...
export $PATH="$HOME/.emacs.d/bin":$PATH"
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
alias e="emacsclient -t -a \"\""
alias ec="emacsclient -c -a \"\""
```

## Reference

-<https://github.com/hlissner/doom-emacs>
-<https://github.com/hlissner/doom-emacs/blob/master/docs/getting_started.org>
-<https://gist.github.com/ecthiender/b9db474e80113bdc18d472de1593eb3c>
