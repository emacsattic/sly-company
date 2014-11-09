sly-company
===========

A [company-mode](http://company-mode.github.io) Emacs completion
backend for [SLY](https://github.com/capitaomorte/sly), a Common Lisp
IDE.

[company-mode](http://company-mode.github.io) is a completion
framework Nikolaj Schumacher. sly-company is based on
[slime-company](https://github.com/anwyn/slime-company).

## Setup

Install via [MELPA](http://melpa.org/#/sly-company), or alternatively
do the following in your `~/.emacs` or `~/.emacs.d/init/el` init file.

```el
(add-to-list 'load-path "/path/to/sly-company")
(require 'sly-company)
```

In either case add this to the init file as well:

```el
(add-hook 'sly-mode-hook 'sly-company-mode)
(add-to-list 'company-backends 'sly-company)

```

The following bindings for `company-active-map` may be useful:

```el
(define-key company-active-map (kbd "\C-n") 'company-select-next)
(define-key company-active-map (kbd "\C-p") 'company-select-previous)
(define-key company-active-map (kbd "\C-d") 'company-show-doc-buffer)
(define-key company-active-map (kbd "M-.") 'company-show-location)
````
