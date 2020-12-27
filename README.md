# Differences with this fork

The only difference is that you can pass additional commands as an argument to i3lock-fancy-rapid. That's it.

Usage: `betterlockscreen_rapid <radius> <times> [command (optional)]`
  
The third argument (optional commands) will be passed to i3lock-fancy-rapid and executed upon unlocking the system.

All other credit goes to the original creator:
https://github.com/oakszyjrnrdy/betterlockscreen_rapid.

# betterlockscreen_rapid

This is a shell script wrapper for [i3lock-fancy-rapid][] inspired by [betterlockscreen][].

It takes a screenshot, blurs it and use it as your lockscreen. All this is done in a very short period of time.

Here is an example:

![screenshot](screenshot.png)

## Feature

- rapid
- good-looking
- configurable

## Installation

### Manual Installation

1. Install all the dependencies.
2. Copy `betterlockscreen_rapid` to `/usr/bin/` or somewhere else in you `$PATH`.
3. Copy `betterlockscreen_rapid.conf` to `/etc/`.

## Configuration

Make directory `$XDG_CONFIG_HOME/betterlockscreen_rapid/` and write your own configuration file `betterlockscreen_rapid.conf` there.

You can use `betterlockscreen_rapid.conf` as a reference. More information can be found at [betterlockscreen][].

Note that `$XDG_CONFIG_HOME` defaults to `$HOME/.config/`.

## Usage

```bash
betterlockscreen_rapid radius times [command (optional)]
```

- `radius` is the kernel size of the box filter.
- `times` is the number of times we filter the image.
- `command (optional)` is the command to be executed upon unlocking the system.

More information can be found at [i3lock-fancy-rapid][].

## Dependency

- [i3lock-color][]
- [i3lock-fancy-rapid][]

## LICENSE

MIT

[i3lock-color]: https://github.com/Raymo111/i3lock-color
[i3lock-fancy-rapid]: https://github.com/yvbbrjdr/i3lock-fancy-rapid
[betterlockscreen]: https://github.com/pavanjadhaw/betterlockscreen
