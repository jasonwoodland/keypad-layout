# Keypad Layout

Control window layout using <kbd>CTRL</kbd> + number keys on macOS. Press two number keys in a row while holding down <kbd>CTRL</kbd> to select the new window position on a 3x3 grid.

This fork adds window spacing and changes the way<kbd>CTRL</kbd>-<kbd>0</kbd> commands work.
<kbd>CTRL</kbd>-<kbd>0</kbd> <kbd>CTRL</kbd>-<kbd>1</kbd>-<kbd>6</kbd> commands now reposition windows on a 3x2 grid.

![Preview](https://github.com/jasonwoodland/keypad-layout/blob/master/Preview.png?raw=true)

## Installation

Download the [latest release](https://github.com/jasonwoodland/keypad-layout/releases/latest) and copy `Keypad Layout.app` to `/Applications`.

You can run Keypad Layout on startup by adding the `plist` to your `LaunchAgents`:

```bash
git clone https://github.com/jasonwoodland/keypad-layout
cp keypad-layout/com.jan-gerd.keypad-layout.plist ~/Library/LaunchAgents
launchctl load -wF ~/Library/LaunchAgents/com.jan-gerd.keypad-layout.plist
```

## Preferences

You can set the window spacing and screen margin while Keypad Layout is running:

```bash
defaults write com.jan-gerd.keypad-layout '{ margin = "{24, 24}"; screenMargin = "{24, 24}"; }'
```

## Examples

| Key Command                                               | Window Position           |
| :-------------------------------------------------------- | :------------------------ |
| <kbd>CTRL</kbd>-<kbd>1</kbd> <kbd>CTRL</kbd>-<kbd>9</kbd> | Full screen               |
| <kbd>CTRL</kbd>-<kbd>7</kbd> <kbd>CTRL</kbd>-<kbd>9</kbd> | Top third                 |
| <kbd>CTRL</kbd>-<kbd>1</kbd> <kbd>CTRL</kbd>-<kbd>3</kbd> | Bottom third              |
| <kbd>CTRL</kbd>-<kbd>3</kbd> <kbd>CTRL</kbd>-<kbd>1</kbd> | Bottom third              |
| <kbd>CTRL</kbd>-<kbd>1</kbd> <kbd>CTRL</kbd>-<kbd>7</kbd> | Left third                |
| <kbd>CTRL</kbd>-<kbd>1</kbd> <kbd>CTRL</kbd>-<kbd>8</kbd> | Left two thirds           |
| <kbd>CTRL</kbd>-<kbd>0</kbd> <kbd>CTRL</kbd>-<kbd>1</kbd> | Bottom half, left third   |
| <kbd>CTRL</kbd>-<kbd>0</kbd> <kbd>CTRL</kbd>-<kbd>2</kbd> | Bottom half, middle third |
| <kbd>CTRL</kbd>-<kbd>0</kbd> <kbd>CTRL</kbd>-<kbd>6</kbd> | Top Half, right third     |
| <kbd>CTRL</kbd>-<kbd>0</kbd> <kbd>CTRL</kbd>-<kbd>7</kbd> | Left half                 |
| <kbd>CTRL</kbd>-<kbd>0</kbd> <kbd>CTRL</kbd>-<kbd>8</kbd> | Full screen               |
| <kbd>CTRL</kbd>-<kbd>0</kbd> <kbd>CTRL</kbd>-<kbd>9</kbd> | Right half                |


## Quit Keypad Layout

```bash
killall Keypad\ Layout
```

## Uninstall

```bash
launchctl unload -wF ~/Library/LaunchAgents/com.jan-gerd.keypad-layout.plist
rm ~/Library/LaunchAgents/com.jan-gerd.keypad-layout.plist
rm -rf /Users/Shared/Keypad\ Layout.app
```

## Attributions
The application and menu bar icons are derived from [numpad](https://thenounproject.com/term/numpad/801826/) by [Ján Slobodník](https://thenounproject.com/janslobodnik/) from the [Noun Project](https://thenounproject.com/), available under the [Creative Commons Attribution](https://creativecommons.org/licenses/by/3.0/us/) license.
