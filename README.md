Lucas.jl
========

Collection of misc. Julia snippets I need more than once.

String handling
===============

strcut
------

```julia
strcut(s, w; dots=true)
```

Function to cut a string `s` into a fixed width `w`. Width means on-sceen width, i.e. while "ที่รัก" has six characters, it's only three characters wide.
If `s` gets cut and `dots` is set to `true`, the last character of the resulting string will be an ellipsis.

strcenter
---------

```julia
strcenter(s, w; dots=true)
```

Centers a string `s` by surrounding it with enough spaces left and right such that it becomes `w` characters wide.
Cuts `s` using `strcut` if it is too long.
