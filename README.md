# bookmarks.kak

A Kakoune plugin for managing bookmarks with position tracking. Inspired by [harpoon.nvim](https://github.com/ThePrimeagen/harpoon/tree/harpoon2) but with added support for cursor position tracking.

The implementation is based on [hadronized/bookmarks.kak](https://github.com/hadronized/bookmarks.kak) and [raiguard/kak-harpoon](https://github.com/raiguard/kak-harpoon).

## Installation

### With [kak-bundle](https://codeberg.org/jdugan6240/kak-bundle)

Add this to your `kakrc`:

```kak
bundle bookmarks "https://github.com/Yukaii/bookmarks.kak" %{
  # Add default keybindings
  bookmarks-add-bindings

  # Or do your own mapping
  map global user m ':bookmarks-add<ret>' -docstring 'add bookmark'
  map global user M ':bookmarks-show-list<ret>' -docstring 'show bookmarks'

  # Different navigation keys
  map global normal <c-1> ':bookmarks-nav 1<ret>'
  map global normal <c-2> ':bookmarks-nav 2<ret>'
  # ... and so on
}
```

### Manual Installation

Clone the repository and source the script in your `kakrc`:

```bash
git clone https://github.com/Yukaii/bookmarks.kak ~/.config/kak/plugins/bookmarks.kak
```

```kak
source "%val{config}/plugins/bookmarks.kak/bookmarks.kak"
bookmarks-init
bookmarks-add-bindings
```

## License

MIT
