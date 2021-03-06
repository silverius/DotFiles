### [Vim](http://www.vim.org/)

#### Install

These are the default instructions using Vim 8's `|packages|` feature. See
sections below, if you use other plugin managers.

1. Create theme folder (in case you don't have yet):

```
mkdir -p ~/.vim/pack/themes/start
```

If you use vim 8.0 (and not 8.2), you may need to use
`~/.vim/pack/themes/opt` instead.

2. Navigate to the folder above:

```
cd ~/.vim/pack/themes/start
```

3. Clone the repository using the "dracula" name:

```
git clone https://github.com/dracula/vim.git dracula
```

4. Create configuration file (in case you don't have yet):

```
touch ~/.vimrc
```

5. Edit the `~/.vimrc` file with the following content:

```
packadd! dracula
syntax enable
colorscheme dracula
```

#### Install using other plugin managers

If you [use vim + pathogen](http://vimcasts.org/episodes/synchronizing-plugins-with-git-submodules-and-pathogen/):

    cd ~/.vim
    git submodule add git@github.com:dracula/vim.git bundle/dracula

Place `colorscheme dracula` after `execute pathogen#infect()`.

If you [use vim + vundle](https://github.com/VundleVim/Vundle):

    Plugin 'dracula/vim', { 'name': 'dracula' }
    :PluginInstall

Place `colorscheme dracula` after `call vundle#end()`.

If you [use vim-plug](https://github.com/junegunn/vim-plug) (\`as\` will install
the plugin in a directory called 'dracula' instead of just 'vim'):

    Plug 'dracula/vim', { 'as': 'dracula' }
    :PlugInstall

Place `colorscheme dracula` after `call plug#end()`.

---

Note that dracula must be in your `'runtimepath'` to load properly: Version 2.0
introduced autoload functionality for part of the plugin, which doesn't work
without `'runtimepath'` properly set. Consult your plugin-managers documentation
to make sure you put dracula on the `'runtimepath'` before loading it.
