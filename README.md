yappyG
======

yappyG is another package for python Git

This a quick and dirty fork of briGit:
Very simple git wrapper module licensed under BSD
Copyright (C) 2011 by Florian Mounier, Kozea


Installation
------------

Use pip :

    pip install git+git://github.com/lucasdurand/yappyg.git

Usage
-----

```python
from yappyg import Git
new_repo = Git("~/brigit/new_repo")  # Will do a git init
git = Git("~/brigit/i_forked_this_from_brigit",
    "git://github.com/lucasdurand/yappyg.git",
     quiet=False)  # Will do a git clone

# Git commands passed through as methods
git.pull()

import os
open(os.path.expanduser("~/brigit/i_forked_this_from_brigit/myNewFile"), "a+").close()
git.add("myNewFile")
# Use *args and **kwargs to pass commands
git.commit("-a", message="Adding myNewFile") # git commit -a --message=
# There's also some utils command:
git.pretty_log()
git.push() # if you have push rights
```
