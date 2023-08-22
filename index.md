---
layout: post
title: AstroNvim Configurations
toc: true
post_style: page
---

<h2>Lazyman Supported AstroNvim Neovim Configurations</h2>

The following are [Lazyman](https://lazyman.dev) supported
[AstroNvim](https://astronvim.com) based Neovim configurations:

| AstroNvim |        |        | Configurations |
| :-------- | :----: | :----: | -------------: |
| [AstroNvimPlus](https://astronvim.lazyman.dev/posts/AstroNvimPlus) | [AstroNvimStart](https://astronvim.lazyman.dev/posts/AstroNvimStart) | [Normal](https://astronvim.lazyman.dev/posts/Normal) | [Micah](https://astronvim.lazyman.dev/posts/Micah) |
| [Kabin](https://astronvim.lazyman.dev/posts/Kabin) | [Lamia](https://astronvim.lazyman.dev/posts/Lamia) | [Orhun](https://astronvim.lazyman.dev/posts/Orhun) | [Spider](https://astronvim.lazyman.dev/posts/Spider) |

Install all Lazyman supported AstroNvim configurations with the command `lazyman -i astronvim`.

## What is AstroNvim

[AstroNvim](https://astronvim.com) is one of the most popular Neovim "distributions"
along with [LazyVim](https://lazyvim.lazyman.dev),
[LunarVim](https://lunarvim.lazyman.dev), and
[NvChad](https://nvchad.lazyman.dev). These aren't really distributions,
they do not include Neovim, but that is what they are called. They are more
accurately described as "Neovim configuration frameworks". In most cases they
provide some pre-configuration of plugins as well as an easy way to extend
the base configuration.

A Neovim configuration framework can be of considerable assistance in managing
the exploding Neovim plugin ecosystem, quickly and easily incorporating
advanced features, and maintaining an up-to-date Neovim configuration.

Features that distinguish AstroNvim include:

- An excellent [community repository](https://github.com/AstroNvim/astrocommunity)
- Fully featured out-of-the-box
- Good documentation

Read our overview and comparison of
[Neovim configuration distributions](https://lazyman.dev/posts/Configuration-Distributions).

## Overview

AstroNvim is an aesthetic and feature-rich neovim config that is extensible
and easy to use with a great set of plugins

## Preview

<kbd><img alt="Preview Image" src="https://astronvim.com/img/themes/overview.png"></kbd>

## Features

- Common plugin specifications with [AstroCommunity](https://github.com/AstroNvim/astrocommunity)
- File explorer with [Neo-tree](https://github.com/nvim-neo-tree/neo-tree.nvim)
- Autocompletion with [Cmp](https://github.com/hrsh7th/nvim-cmp)
- Git integration with [Gitsigns](https://github.com/lewis6991/gitsigns.nvim)
- Statusline, Winbar, and Bufferline with [Heirline](https://github.com/rebelot/heirline.nvim)
- Terminal with [Toggleterm](https://github.com/akinsho/toggleterm.nvim)
- Fuzzy finding with [Telescope](https://github.com/nvim-telescope/telescope.nvim)
- Syntax highlighting with [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- Formatting and Linting with [Null-ls](https://github.com/jose-elias-alvarez/null-ls.nvim)
- Language Server Protocol with [Native LSP](https://github.com/neovim/nvim-lspconfig)
- Debug Adapter Protocol with [nvim-dap](https://github.com/mfussenegger/nvim-dap)

## Requirements

- [Nerd Fonts](https://www.nerdfonts.com/font-downloads) (_Optional with manual intervention:_ See [Documentation on customizing icons](https://astronvim.com/Recipes/icons))
- [Neovim 0.8+ (_Not_ including nightly)](https://github.com/neovim/neovim/releases/tag/stable)
- [Tree-sitter CLI](https://github.com/tree-sitter/tree-sitter/blob/master/cli/README.md) (_Note:_ This is only necessary if you want to use `auto_install` feature with Treesitter)
- A clipboard tool is necessary for the integration with the system clipboard (see [`:help clipboard-tool`](https://neovim.io/doc/user/provider.html#clipboard-tool) for supported solutions)
- Terminal with true color support (for the default theme, otherwise it is dependent on the theme you are using)
- Optional Requirements:
  - [ripgrep](https://github.com/BurntSushi/ripgrep) - live grep telescope search (`<leader>fw`)
  - [lazygit](https://github.com/jesseduffield/lazygit) - git ui toggle terminal (`<leader>tl` or `<leader>gg`)
  - [go DiskUsage()](https://github.com/dundee/gdu) - disk usage toggle terminal (`<leader>tu`)
  - [bottom](https://github.com/ClementTsang/bottom) - process viewer toggle terminal (`<leader>tt`)
  - [Python](https://www.python.org/) - python repl toggle terminal (`<leader>tp`)
  - [Node](https://nodejs.org/en/) - node repl toggle terminal (`<leader>tn`)

## Community Plugin Configurations

One of the strongest features of AsroNvim is the community-provided setups from
the [AstroCommunity repository](https://github.com/AstroNvim/astrocommunity).
This is a repository of many many preconfigured Neovim plugins ready to easily
incorporate in an AstroNvim based configuration.

For example, to enable language tools (LSP and DAP etc.) for Rust and Python,
your `plugins/community.lua` file can look like the following:

```lua
return {
  -- Add the community repository of plugin specifications
  "AstroNvim/astrocommunity",
  -- example of importing a plugin, comment out to use it or add your own
  -- available plugins can be found at https://github.com/AstroNvim/astrocommunity
  -- { import = "astrocommunity.colorscheme.catppuccin" },
  { import = "astrocommunity.pack.rust" },
  { import = "astrocommunity.pack.python" },
}
```

<div align="center">
  <p align="center">
    <a href="https://ronrecord.com" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="domain"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/domain.png"
    /></a>
    <a href="https://www.reddit.com/user/No-Blackberry-3160" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="reddit"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/reddit.png"
    /></a>
    <a href="https://github.com/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="github"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/github.png"
    /></a>
    <a href="https://gitlab.com/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="gitlab"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/gitlab.png"
    /></a>
    <a href="https://twitter.com/ronrecord" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="twitter"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/twitter.png"
    /></a>
    <a href="https://youtube.com/c/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="youtube"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/youtube.png"
    /></a>
    <a href="https://linkedin.com/in/ronrecord" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="linkedin"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/linkedin.png"
    /></a>
    <a href="https://instagram.com/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="instagram"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/instagram.png"
    /></a>
    <a href="https://noc.social/@doctorwhen" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="mastodon"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/mastodon.png"
    /></a>
    <a href="https://en.wikipedia.org/wiki/User:Doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="wikipedia"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/wikipedia.png"
    /></a>
  </p>
</div>
