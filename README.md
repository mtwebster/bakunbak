Simple tool to let you backup or restore files and folders by adding and removing a '.bak' suffix to the original filename.

Because I get sick of typing this manually.

Use bak (or unbak) --help to see how to use it.

Build (requires meson):

```
meson builddir        (--prefix= optional)
ninja -C builddir
sudo ninja -C builddir install
```

