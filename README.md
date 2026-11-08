# goda-term-ui-terminal.vim

The UI `terminal` of
[goda-term.vim](https://github.com/Shougo/goda-term.vim): a terminal job of
Vim or Neovim (ddt-ui-terminal).

## Requirements

- [goda-term.vim](https://github.com/Shougo/goda-term.vim)

## Usage

Add it to the configuration of goda-term.vim:

```go
import "github.com/Shougo/goda-term-ui-terminal.vim/ext/ui/terminal"

b.AddUI(terminal.New())
```

Then:

```vim
nnoremap [Space]t <Cmd>call goda_term#start(#{
      \   name: t:->get('goda_term_ui_terminal_last_name',
      \                 'terminal-' .. win_getid()),
      \   ui: 'terminal',
      \ })<CR>
```

See `:help goda-term-ui-terminal`.
