Dart Mode
=========
Dart Mode is a major mode for editing Dart files in Emacs.

## Installation

1. Add [Marmalade](https://marmalade-repo.org/#download) to your
   `package-archives` if you don't already have it.

1.  Install dart-mode via:
    ```
    M-x package-refresh-contents [RET]
    M-x package-install [RET] dart-mode
    ```

1.  OPTIONAL: To enable on-the-fly syntax checking, add the
    following to your `.emacs` file:
    ```
    (setq dart-enable-analysis-server t)
    (add-hook 'dart-mode-hook 'flycheck-mode)
    ```

1.  OPTIONAL: To enable imenu support, add the
    following to your `.emacs` file:
    ```
	(add-hook 'dart-mode-hook
          (lambda ()
            (setq imenu-create-index-function #'dart-imenu-index)))
    ```
1.  OPTIONAL: To view the class hierarchy install tree-mode

1.  Features & functions: Provides the following functions
    1. dart-format-file: can be called on a save file hook
    2. dart-jump-to-defn: bind to a key and navigate source code
    3. dart-type-hierarchy: bind to a key and show the type hierachy
    4. dart-hover-information: bind to key and show dartdocs for the element
    5. dart-imports: sort import directives
    6. dart-sort-members: sort all imports
    7. dart-quick-fix: apply quick fix

1. Use [company-dart] (https://github.com/sid-kurias/company-dart) to get intellisense
   like support.
