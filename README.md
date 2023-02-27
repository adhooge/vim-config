
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

## LaTeX

Be sure to have LaTeX installed beforehand:

```bash
sudo apt install texlive
```

By default, building is done using `latexmk`. It can be installed with:

```bash
sudo apt install latexmk
```

Using `Texlab` which is directly available through `coc-texlab`:

```Vim
:CocInstall coc-texlab
```

Texlab should be downloaded automatically from [GitHub](https://github.com/latex-lsp/texlab)

While editing a Tex Document, it is then possible to build it with:

```Vim
:CocInstall latex.Build
```

To automatically build after saving, set `texlab.build.onSave` to `true` in `:CocConfig`.

The previewer also needs to be set for it to update automatically and
open on save. To do so, set the following arguments in `:CocConfig`:

```json
"texlab.forwardSearch.executable": "okular",
"texlab.forwardSearch.arguments": ["--unique", "file:%p#src:%l%f"]
```

To enable forward search (syncing .tex file and .pdf), enable the following parameter:

```json
"texlab.build.forwardSearchAfter": true
```

