# .DOT. -DASH-

To install, just copy `dot_files/` to your `$HOME` directory and then symlink the `bash/bashrc` file to `~/.bashrc` and `git/gitconfig` to `~/.gitconfig`:

```{.bash}
  ln -s ~/dot_files/bash/bashrc ~/.bashrc
  ln -s ~/dot_files/git/gitconfig ~/.gitconfig
```

If that doesn't work, check that your `~/.bashrc` file is being sourced (by `~/.profile`) when you start a session.

To get `vim` up and running, clone the `Plug` (<https://github.com/junegunn/vim-plug>) GitHub repository and then run :PlugInstall.
Full instructions can be found in the `dot_files/vim/vimrc` file.


## Windows

In order to get a sane terminal install wintty.

Then copy `windows/mintty/config` to `%APPDATA%/wsltty/config`

Then copy the contents of `windows\mintty\base16-mintty\mintty/` to `%APPDATA%/wsltty/themes/`

Finally, run `windows/capslock_to_ctrl.reg` to remap the capslock key to control in Windows.

