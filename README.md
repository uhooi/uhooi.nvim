# uhooi.nvim

Blazingly fast implementation for UHOOI with Neovim Lua.

https://user-images.githubusercontent.com/21194714/177351810-f84d0363-426f-4826-b9ae-e93163cdf682.mov

## What's this?

This is a fork of [delphinus/nekokak.nvim][] that replaced Nekokak with Uhooi.

[delphinus/nekokak.nvim]: https://github.com/delphinus/nekokak.nvim

## Requirements

- Terminal: support True Color
  - e.g. [iTerm2][]
- Run `:set termguicolors`

[iTerm2]: https://iterm2.com/

## Installation

### for [packer.nvim][]

```lua
use {
  "uhooi/uhooi.nvim",
  config = function()
    require "uhooi".setup {}
  end,
}
```

[packer.nvim]: https://github.com/wbthomason/packer.nvim

### for [Dein.vim][]

```toml
[[plugins]]
repo = 'uhooi/uhooi.nvim'
if = "has('nvim')"
```

```shell
:lua require "uhooi".setup {}
```

[Dein.vim]: https://github.com/Shougo/dein.vim

### for builtin [packages][]

```sh
git clone https://github.com/uhooi/uhooi.nvim \
  $HOME/.local/share/nvim/site/pack/foobar/start/uhooi.nvim
```

```lua
-- And in your init.lua……
require "uhooi".setup {}
```

[packages]: https://neovim.io/doc/user/repeat.html#packages

## Commands

### `Uhooi`

```vim
:Uhooi
```

You see him.

```vim
:Uhooi { wait_ms = 10, direction = 'loop' }
```

You see more passionate him.

#### Options

* `wait_ms` (default: `100`)
  - Milliseconds to wait between frames.
* `direction` (default: `'expand'`)
  - Direction to animate him. Either `'expand'`, `'reduct'` or `'loop'` is available.
* `count` (default: `3`)
  - Count to loop. This is ignored when `direction` is not `'loop'`.

## Functions

### `start(opts)`

You can start UHOOI.

```lua
:lua require "uhooi".start { wait_ms = 10, direction = 'loop' }
```

`opts` are the same one as for `:Uhooi`.

## See also

* [delphinus/nekokak.nvim][]
