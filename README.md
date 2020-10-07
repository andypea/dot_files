# .DOT. -DASH-

To install, just copy `dot_files/` to your `$HOME` directory and then symlink the `bash/bashrc` file to ~/.bashrc:

```{.bash}
  ln -s ~/dot_files/bash/bashrc ~/.bashrc
```

If that doesn't work, check that your `~/.bashrc` file is being sourced (by `~/.profile`) when you start a session.

To get `vim` up and running, clone the `Plug` <https://github.com/junegunn/vim-plug> GitHub repository and then run :PlugInstall.
Full instructions can be found in the `dot_files/vim/vimrc` file.


## Windows

In order to get a sane terminal install wintty.

