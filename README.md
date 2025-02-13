# `org-context`

Allows saving the context of an Org-mode entry, such as when refiling, so that
entries can be restored to their original location based on that context.

Here is the configuration I am using:
```elisp
(use-package org-context
  :after org
  :demand t
  :bind (:map
         org-mode-map
         ("C-c C-x R" . org-context-undo)
         ("C-c C-x W" . org-context-show-olpath))
  :config
  (org-context-install))
```
