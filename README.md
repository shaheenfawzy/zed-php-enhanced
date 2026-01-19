# PHP Enhanced for Zed

Enhanced PHP syntax highlighting for [Zed](https://zed.dev) with colored built-in functions, magic methods, and improved operator highlighting.

## Features

- **1685+ PHP built-in functions** highlighted distinctly (uses `@label` capture - green with Night Owl Black theme)
- **Magic methods** (`__construct`, `__invoke`, `__toString`, etc.) highlighted
- **Enhanced operator highlighting** for `=>`, `->`, `::`, `?->`
- **`$this` special highlighting** (uses `@variable.special` capture)
- Works with **any Zed theme** (colors depend on theme's token colors)

## Installation

1. Open Zed
2. Open the Extensions panel (`cmd+shift+x` on macOS, `ctrl+shift+x` on Linux)
3. Search for "PHP Enhanced"
4. Click Install

**Note:** This extension replaces Zed's built-in PHP syntax highlighting. If you want to revert, simply uninstall this extension.

## What Gets Highlighted

### Built-in Functions (Sample)

The following categories of PHP functions are highlighted:

- **Array functions**: `array_map`, `array_filter`, `array_merge`, `array_keys`, etc.
- **String functions**: `strlen`, `strpos`, `str_replace`, `explode`, `implode`, etc.
- **File functions**: `file_get_contents`, `file_put_contents`, `fopen`, `fclose`, etc.
- **JSON functions**: `json_encode`, `json_decode`, `json_validate`, etc.
- **Database functions**: `mysqli_*`, `pdo_*` functions
- **Date/Time functions**: `date`, `time`, `strtotime`, `mktime`, etc.
- **Regular expressions**: `preg_match`, `preg_replace`, `preg_split`, etc.
- **And many more...**

### Magic Methods

All PHP magic methods are highlighted:
- `__construct`, `__destruct`
- `__get`, `__set`, `__isset`, `__unset`
- `__call`, `__callStatic`
- `__invoke`, `__toString`, `__debugInfo`
- `__sleep`, `__wakeup`, `__serialize`, `__unserialize`
- `__clone`, `__set_state`

## Theme Compatibility

This extension uses standard Tree-sitter capture names that work with any Zed theme:

| Element | Capture | Example Color (Night Owl Black) |
|---------|---------|--------------------------------|
| Built-in functions | `@label` | Green (`#addb67`) |
| Magic methods | `@label` | Green (`#addb67`) |
| `$this` | `@variable.special` | Cyan (`#7fdbca`) |
| User functions | `@function` | Blue (`#82aaff`) |
| Operators | `@operator` | Cyan (`#7fdbca`) |

## Companion Theme

For the best experience, pair with:
- [Night Owl Black](https://github.com/shaheenfawzy/zed-night-owl-black) - A pure black variant of Night Owl

## Credits

- Built on top of the [tree-sitter-php](https://github.com/tree-sitter/tree-sitter-php) grammar
- PHP function list generated from `get_defined_functions()['internal']`

## License

MIT License - see [LICENSE](LICENSE) for details.
