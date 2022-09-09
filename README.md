# ob-babashka

Modified from this [gist](https://gist.github.com/lasvice/aad29c970f1c221d5663286a0fbd0ad8) which in turns modified from https://github.com/emacsmirror/ob-clojurescript/blob/master/ob-clojurescript.el

## Installation
Just for personal use, so currently not published to Melpha.
Install with [use-package](https://github.com/jwiegley/use-package) with [straight.el](https://github.com/radian-software/straight.el):
```emacs-lisp
(use-package ob-babashka
  :straight (:type git :host github :repo "lasvice/ob-babashka"))
(use-package org
  :straight (:type built-in)
  :config
  (org-babel-do-load-languages
   'org-babel-load-languages
   '(
      ;; other languages
      ;; ...
      (babashka . t))))
```

## Usage

```org
#+begin_src bb
  (def n 40)
  (+ n 2)
#+end_src
```

