*format-all* for Emacs
======================

What does it do
---------------

Lets you auto-format source code in many languages using the same
command for all languages, instead of learning a different elisp
package and formatting command for each language. Just do **M-x**
`format-all-buffer` and it will try its best to do the right thing.

Supported languages
-------------------

* **C/C++/Objective-C** ([*clang-format*](https://clang.llvm.org/docs/ClangFormat.html))
* **CSS/Less/SCSS** ([*prettier*](https://prettier.io/))
* **D** ([*dfmt*](https://github.com/dlang-community/dfmt))
* **Elixir** ([*mix format*](https://hexdocs.pm/mix/master/Mix.Tasks.Format.html))
* **Elm** ([*elm-format*](https://github.com/avh4/elm-format))
* **Emacs Lisp** (native)
* **Go** ([*gofmt*](https://golang.org/cmd/gofmt/))
* **GraphQL** ([*prettier*](https://prettier.io/))
* **Haskell** ([*hindent*](https://github.com/commercialhaskell/hindent))
* **HTML/XHTML/XML** ([*tidy*](http://www.html-tidy.org/))
* **Java** ([*clang-format*](https://clang.llvm.org/docs/ClangFormat.html))
* **JavaScript/JSON/JSX/TypeScript/Vue** ([*prettier*](https://prettier.io/))
* **Kotlin** ([*ktlint*](https://github.com/shyiko/ktlint))
* **Markdown** ([*prettier*](https://prettier.io/))
* **OCaml** ([*ocp-indent*](https://opam.ocaml.org/packages/ocp-indent/))
* **Perl** ([*perltidy*](http://perltidy.sourceforge.net/))
* **Protocol Buffers** ([*clang-format*](https://clang.llvm.org/docs/ClangFormat.html))
* **Python** ([*autopep8*](https://pypi.org/project/autopep8/))
* **Ruby** ([*rufo*](https://github.com/ruby-formatter/rufo))
* **Rust** ([*rustfmt*](https://github.com/rust-lang-nursery/rustfmt))
* **Shell script** ([*shfmt*](https://github.com/mvdan/sh))
* **SQL** ([*sqlformat*](https://pypi.org/project/sqlparse/))
* **Swift** ([*swiftformat*](https://github.com/nicklockwood/SwiftFormat))

How to install
--------------

From [MELPA](https://melpa.org/#/?q=format-all)

You will need to install external programs to do the formatting. If
`format-all-buffer` can't find the right program, it will try to tell
you how to install it.

How to customize
----------------

A local minor mode called `format-all-mode` is available to format
code on save. Please see the documentation for that function for
instructions.

There are currently no customize variables, since it's not clear what
approach should be taken. Please see [GitHub issues][github-issues]
for discussion.

Many of the external formatters support configuration files in the
source code directory to control their formatting. Please see the
documentation for each formatter.

How to add new languages
------------------------

New external formatters can be added easily if they can read code from
standard input and format it to standard output. Feel free to submit a
pull request or ask for help in [GitHub issues][github-issues].

How to report bugs
------------------

[GitHub issues][github-issues] are preferred. Email is also ok.

Feature requests are welcome. If you are interested in doing anything
beyong just adding new formatters in the current framework, please
discuss in issues before writing code, since there are big unresolved
questions about where the project should go from here.

Roadmap
-------

**[atom-beautify](https://atom.io/packages/atom-beautify#beautifiers)**
sports a very impressive set of formatters. We should aspire to that
level of coverage for Emacs.

**[Unibeautify](https://github.com/Unibeautify/unibeautify)** is a
project to provide one shell command to run all beautifiers.
*atom-beautify* will be rewritten to be based on it. Perhaps we should
be too, once it stabilizes.

[github-issues]: https://github.com/lassik/emacs-format-all-the-code/issues
