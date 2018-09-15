Calm Spring Color Scheme for Vim [![Build Status][]][Travis CI]
===============================================================

`spring-night` is a low contrast calm color scheme for Vim. It's colored with deep blue background,
shiny yellow foreground and *sakura*:cherry_blossom: text selection.

- Both GUI/CUI 24bit colors and CUI 256 colors.
- Aware of running Vim on translucent window.
- Enable to tweak contrast.
- Optimized for many filetypes.
- Support [vim-gitgutter][] and other several plugins.
- Support Neovim/Vim (8.0.1685 or later) terminal ANSI colors.


## On gVim (MacVim)

| Vim script                       | Go                       |
|----------------------------------|--------------------------|
| ![Vim script on gVim (MacVim)][] | ![Go on gVim (MacVim)][] |


## On Translucent Terminal (24bit color)

| Vim script                           | Go                           |
|--------------------------------------|------------------------------|
| ![Vim script on Vim (24bit color)][] | ![Go on Vim (24bit color)][] |


## On Translucent Terminal (8bit color)

| Vim script                          | Go                          |
|-------------------------------------|-----------------------------|
| ![Vim script on Vim (8bit color)][] | ![Go on Vim (8bit color)][] |

If you want to see more code, please visit [demo page site][].


## Installation

Copy `colors` directory into your `~/.vim` (or `~/vimfiles` on Windows) or use `:packadd` (Vim8).
Or use your favorite plugin manager.


## Usage

Write below in your `.vimrc`.

```vim
colorscheme spring-night
```

This package provides a theme for [vim-airline][].

```vim
let g:airline_theme = 'spring_night'
```

If you want to use 24bit colors on Vim in a terminal window, you also need to set `termguicolors`
option. Please note that it requires a ISO-8613-3 compatible terminal to enable 24bit colors.

```vim
" For Vim 7.4.1799 or later
if has('termguicolors')
    let &t_8f = "\<Esc>[38;2;%lu;%lu;%lum"
    let &t_8b = "\<Esc>[48;2;%lu;%lu;%lum"
    set termguicolors
endif

" For Neovim 0.1.5 or later
set termguicolors
```


## Customize

You can customize some behaviors of this colorscheme. Please note that these variable must be
specified before running `:colorscheme`.

- **`g:spring_night_kill_italic`**: If `1`, this colorscheme does not use italic attribute. Default value is `0`.
- **`g:spring_night_kill_bold`**: If `1`, this colorscheme does not use bold attribute. Default value is `0`.
- **`g:spring_night_high_contrast`**: If `1`, it uses a bit high contrast colors. Default value depends on
  `termguicolors` option and whether on GUI or CUI Vim is running.
- **`g:spring_night_highlight_terminal`**: If `1`, a terminal window is also highlighted with this color
  scheme. Otherwise default ANSI colors are used. Default value is `1`.
- `g:spring_night_cterm_italic`: If `1`, italic font is enabled even in a terminal. This variable is
  useful when your terminal supports italic fonts. Default value is `0`.


## Optimized Filetypes and Plugins

Color layouts are optimized for following filetypes/plugins:

- `c`
- `cpp`
- `diff`
- `gitcommit`
- `go`
- `help`
- `html`
- `javascript`
- `markdown`
- `ocaml`
- `python`
- `rst`
- `ruby`
- `rust`
- `typescript`
- `vim`
- `wast`
- `zsh`
- [ctrlp][]
- [vim-gitgutter][]
- [vim-easymotion][]
- [clever-f.vim][]
- [vimfiler.vim][]
- [ale][]
- [vim-highlightedyank][]
- ... and more


## Contribution

If you find some odd highlight, I'll be happy if you report it to
[issues](https://github.com/rhysd/vim-color-spring-night/issues/new) with how to reproduce.
And pull requests are of course welcome :smile:

Colorscheme file is generated via [a script](gen/src/main.rs). Please do not modify
`spring_night.vim` directly. Modify the script instead. Please read [a README for the script](gen/README.md)
for more details.
To know colors palette, please see `table` variable in `spring_night_writer()` function in the script.


## Bonus: Slack Theme

```
#132132,#3a4b5c,#fedf81,#132132,#8090a0,#fffeeb,#a9dd9d,#a9667a
```


## License

Licensed under the MIT license.

```
MIT License

Copyright (c) 2016 rhysd

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR
THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

[demo page site]: https://rhysd.github.io/vim-color-spring-night
[vim-airline]: https://github.com/vim-airline/vim-airline
[vim-gitgutter]: https://github.com/airblade/vim-gitgutter
[ctrlp]: https://github.com/ctrlpvim/ctrlp.vim
[vim-easymotion]: https://github.com/easymotion/vim-easymotion
[Vim script on gVim (MacVim)]: https://github.com/rhysd/ss/blob/master/vim-color-spring-night/gui-vim.jpg?raw=true
[Go on gVim (MacVim)]: https://github.com/rhysd/ss/blob/master/vim-color-spring-night/gui-go.jpg?raw=true
[Vim script on Vim (24bit color)]: https://github.com/rhysd/ss/blob/master/vim-color-spring-night/terminal-64bit-vim.jpg?raw=true
[Go on Vim (24bit color)]: https://github.com/rhysd/ss/blob/master/vim-color-spring-night/terminal-64bit-go.jpg?raw=true
[Vim script on Vim (8bit color)]: https://github.com/rhysd/ss/blob/master/vim-color-spring-night/terminal-8bit-vim.jpg?raw=true
[Go on Vim (8bit color)]: https://github.com/rhysd/ss/blob/master/vim-color-spring-night/terminal-8bit-go.jpg?raw=true
[Build Status]: https://travis-ci.org/rhysd/vim-color-spring-night.svg?branch=travis
[Travis CI]: https://travis-ci.org/rhysd/vim-color-spring-night
[clever-f.vim]: https://github.com/rhysd/clever-f.vim
[vimfiler.vim]: https://github.com/Shougo/vimfiler.vim
[ale]: https://github.com/w0rp/ale
[vim-highlightedyank]: https://github.com/machakann/vim-highlightedyank
