Color.lua - ANSI control library for Lua
========================================

A super-simple way to make colored text output in Lua.
To use, simply print out things from this module, then print out some text.

Examples:
----------

```lua
print(color.bg.green .. color.fg.RED .. "This is bright red on green")

print(color.invert .. "This is inverted..." .. color.reset .. " And this isn't.")

print(color.fg(0xDE) .. color.bg(0xEE) ..
    "You can use xterm-256 colors too!" ..
    color.reset)

print("And also " .. color.bold .. "BOLD" .. color.normal .. " if you want.")

print(color.bold .. color.fg.BLUE .. color.bg.blue ..
    "Miss your " .. color.fg.RED .. "C-64" ..
    color.fg.BLUE .. "?" .. color.reset)
```

You can see all these examples in action by calling `color.test()`

Can't pick a good color scheme? Look at a handy chart:

```lua
print(color.chart())
```

Extending:
----------

I figured out most of how to write this from the excellent [Wikipedia page on ANSI control codes](http://en.wikipedia.org/wiki/ANSI_escape_code). If you want to extend it, that would be a good place to start. And send me a pull request!

Portability:
-----------

This doesn't work on Windows at all, and it would be a really nontrivial effort to port it.

License:
----------

Copyright 2012 by Ross Andrews, released under the [GNU Lesser General Public License](http://www.gnu.org/licenses/lgpl.txt).