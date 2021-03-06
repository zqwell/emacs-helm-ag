# helm-ag.el

## Introduction
`helm-ag.el` provides interfaces of [the silver searcher](https://github.com/ggreer/the_silver_searcher) with helm.


## Screenshot

![helm-ag](image/helm-ag.png)


## Requirements

* Emacs 24 or higher
* helm 1.0 or higher
* [the silver searcher](https://github.com/ggreer/the_silver_searcher).


## Basic Usage

Input search word with `ag` command. You can change search directory
with `C-u` prefix.

    M-x helm-ag

Same as `helm-ag` except to search only current file

    M-x helm-ag-this-file

Move to point before jump

    M-x helm-ag-pop-stack

Clear context stack

    M-x helm-ag-pop-stack


## Persistent action

You can see file content temporarily by persistent action(`C-z`)
at `helm-ag` and `helm-ag-this-file`.


## Customize

Base ag command, default is `ag --nocolor --nogroup`

    (setq helm-ag-base-command "ag --nocolor --nogroup --ignore-case")

Command line option of base command. Default is `nil`.

    (setq helm-ag-command-option "--all-text")

Insert thing at point as default search pattern, if this value is `non nil`.
You can set parameter same as `thing-at-point`(Such as `'word`, `symbol` etc).
Default value is `nil`.

    (setq helm-ag-thing-at-point 'symbol)
