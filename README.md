# cinder-grove.el

A warm, muted Emacs theme that's easy on the eyes.

![Showcase](./assets/screenshot.png)

## Ports

- [Neovim](https://github.com/aileks/cinder-grove.nvim)
- [VS Code](https://github.com/aileks/cinder-grove)
- [GTK](https://github.com/aileks/cinder-grove-gtk)

## Features

- Built-in faces: editing, search, completions, dired, info, ediff, smerge, whitespace, compilation, and more
- Full font-lock coverage including the Emacs 29/30 faces used by tree-sitter major modes
- Org (with Doom's extra todo faces) and Markdown
- Package faces for corfu, vertico, marginalia, orderless, consult, and embark
- Git and diff: magit, diff-hl, ediff, smerge, and git-timemachine
- Diagnostics for flycheck and flymake
- lsp-mode: highlights, breadcrumbs, inlay hints, and semantic tokens
- Doom Emacs surroundings: doom-modeline, solaire, dashboard, which-key, hl-todo, nav-flash, indent-bars, transient, avy, ace-window, anzu, and evil plugins (goggles, snipe, traces)
- diredfl, dirvish, and nerd-icons
- vterm and term with the Cinder Grove ANSI palette
- Optional transparency
- Theme faces are inert for packages that aren't installed, so no setup beyond loading the theme is needed

## Installation

Doom Emacs (`packages.el` and `config.el`):

```elisp
(package! cinder-grove :recipe (:host github :repo "aileks/cinder-grove.el"))
```

```elisp
(setq doom-theme 'cinder-grove)
```

use-package with straight.el:

```elisp
(use-package cinder-grove-theme
  :straight (:host github :repo "aileks/cinder-grove.el")
  :config (load-theme 'cinder-grove t))
```

Manually, after cloning the repository:

```elisp
(add-to-list 'custom-theme-load-path "/path/to/cinder-grove.el")
(load-theme 'cinder-grove t)
```

Or copy `cinder-grove-theme.el` into `~/.emacs.d/themes/` (or `$DOOMDIR/themes/` in Doom) and load it from there.

## Configuration

Enable transparency while keeping floating windows opaque:

```elisp
(setq cinder-grove-transparent t)
(load-theme 'cinder-grove t)
```

In terminal Emacs the terminal's background shows through. In GUI, add a frame `alpha-background` for real see-through (Emacs 29+); without one, transparent mode looks the same as opaque:

```elisp
(add-to-list 'default-frame-alist '(alpha-background . 85))
```

## Palette

![Cinder Grove color palette](./assets/palette.svg)

## License

[GPL-3.0-or-later](./LICENSE)
