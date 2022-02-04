# BacklightFixup
A "fix" for Penryn-based MacBook keyboard backlight in macOS Big Sur and Monterey


# What this does:
BacklightFixup starts an instance of TouchBarServer, which seems to talk with `corebrightnessd` in such a way that fixes keyboard backlight on Penryn-based Macs.

The reasoning for why this works is still relatively unknown, but is being looked into by more knowledgeable people within @moraea and @dortania.

BacklightFixup.dylib is injected into a process (loginwindow, typically), and when this process is started, it will launch TouchBarServer.


# How it works
Something with how TouchBarServer talks with `corebrightnessd`

