
# vim-config

My Vim configuration for coding

## Markdown

### Linting

Linting is done with `coc-nvim`. Run the following command:

```Vim
:CocInstall coc-markdownlint
```

### Preview

Automatic preview is enabled by [instant-markdown](https://github.com/instant-markdown/vim-instant-markdown).
Add this line to `.vimrc`:

```Vim
Plug 'instant-markdown/vim-instant-markdown', {'for': 'markdown', 'do': 'yarn install'}
```

Then install the plugin with `:PlugInstall`.
