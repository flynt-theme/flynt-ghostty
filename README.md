# Flynt for Ghostty

Warm tones. Zero visual noise. - [Flynt](https://flynt-theme.github.io/flynt) for [Ghostty](https://ghostty.org).

## Install

### 1. Copy theme files

**macOS** - Ghostty stores user themes in Application Support:
```sh
mkdir -p ~/Library/Application\ Support/com.mitchellh.ghostty/themes
cp dist/flynt-dark ~/Library/Application\ Support/com.mitchellh.ghostty/themes/
cp dist/flynt-light ~/Library/Application\ Support/com.mitchellh.ghostty/themes/
```

**Linux** - Ghostty uses the XDG config directory:
```sh
mkdir -p ~/.config/ghostty/themes
cp dist/flynt-dark ~/.config/ghostty/themes/
cp dist/flynt-light ~/.config/ghostty/themes/
```

### 2. Set the theme

Open your Ghostty config and add:

```
theme = light:flynt-light,dark:flynt-dark
```

Ghostty switches automatically based on your OS light/dark mode. To pin a single variant:

```
theme = flynt-dark
```

**Config file locations** (Ghostty loads all that exist, later files override earlier ones):

| Platform | Path |
|----------|------|
| All platforms (XDG) | `~/.config/ghostty/config.ghostty` |
| macOS (App Support) | `~/Library/Application Support/com.mitchellh.ghostty/config.ghostty` |

On macOS, Ghostty creates the config in Application Support by default. After editing, reload with **Cmd+Shift+,** or restart Ghostty.

## Building from source

Themes are generated from [`theme.conf.tmpl`](theme.conf.tmpl) using [strike](https://github.com/flynt-theme/strike).

```sh
brew tap flynt-theme/tap && brew install strike
strike build theme.conf.tmpl --out dist/
```

## License

MIT - [Flynt Theme](https://github.com/flynt-theme)
