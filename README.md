# blamer.nvim

A git blame plugin for neovim inspired by VS Code's GitLens plugin.

## Installation

#### vim-plug

1. Add the following line to your `init.vim`:

```
call plug#begin('~/.local/share/nvim/plugged')
...
Plug 'APZelos/blamer.nvim'
...
call plug#end()
```

2. Run `:PlugInstall`.

## Configuration

#### Enabled

Enables blamer on neovim startup.

You can toggle blamer on/off with the `:BlamerToggle` command.

If the current directory is not a git repository the blamer will be automatically disabled.

Default: `0`

```
let g:blamer_enabled = 1
```

#### Delay

The delay in milliseconds for the blame message to show. Setting this too low may cause performance issues.

Default: `1000`

```
let g:blamer_delay = 500
```

#### Prefix

The prefix that will be added to the template.

Default: `' '`

```
let g:blamer_prefix = ' > '
```

#### Template

The template for the blame message that will be shown.

Default: `'<committer>, <committer-time> • <summary>'`

Available options: `<author>`, `<author-mail>`, `<author-time>`, `<committer>`, `<committer-mail>`, `<committer-time>`, `<summary>`.

```
let g:blamer_template = '<committer> <summary>'
```

#### Highlight

The color of the blame message.

Default: `link Blamer Comment`

```
highlight Blamer guifg=lightgrey
```

## Author

[APZelos](https://github.com/APZelos)

## License

This software is released under the MIT License.
