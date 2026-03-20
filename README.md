# Simple EXecutable Ini (SEXI)
This is a very simple tool which can launch an .exe using Wine, Proton or UMU-Launcher by storing the corresponding
settings in an ini file which you keep immediately next to the .exe.

If you give the .ini files the .sexi file extension and assign that file extension a custom mime type (e.g. text/sexi)
you can associate that with SEXI, and then double-clicking the .sexi file will launch the game.

You can do the same with your text editor (e.g. Kate) so that if you open the .sexi file with Kate it gets treated like
a normal .ini file for syntax highlighting.

This is currently an early prototype. Consider it to be a proof-of-concept. I might add more features. Maybe.

## Why I made this
I have a large number of copy-pasteable Windows games, many of which are quite old. My normal method for getting these
running on a new computer is to copy them, paste them, double-click the .exe and it just works. I wanted to replicate
this on Linux, so that I can double-click the .sexi and it just works.

## Examples
Just look how simple it is to use!

#### Raptor
```ini
[main]
prefix = /opt/_pfx/gamemaker
compatibility_tool = umu
runner_version = GE-Proton9-27
program = Raptor.exe
```

#### Warcraft III The Frozen Throne
```ini
[main]
prefix = /opt/_pfx/wc3
compatibility_tool = proton
runner_version = GE-Proton9-27
program = Frozen Throne.exe
arguments = -window

[env]
WINEDLLOVERRIDES=d3d8=n
```

#### World of Warcraft
```ini
[main]
prefix = /opt/_pfx/wow
compatibility_tool = proton
runner_version = GE-Proton9-27
program = Wow.exe
```

## License
Licensed under the MIT license.
