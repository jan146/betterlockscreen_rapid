# Differences with this fork

* Execute commands before locking the system
* Execute commands after unlocking the system
* Set default radius and times parameters

Installation and usage sections have been updated accordingly.

All other credit goes to the original creator:
https://github.com/oakszyjrnrdy/betterlockscreen_rapid.

# betterlockscreen_rapid

This is a shell script wrapper for [i3lock-fancy-rapid][] inspired by [betterlockscreen][].

It takes a screenshot, blurs it and use it as your lockscreen. All this is done in a very short period of time.

Here is an example:

![screenshot](screenshot.png)

## Features

* Rapid
* Good-looking
* Configurable

## Installation

Before installing, make sure you have all the dependencies already installed (listed at the bottom of the page).
Then run the following commands in your terminal:

```
git clone https://github.com/jan146/betterlockscreen_rapid.git
cd betterlockscreen_rapid
sudo ./install.sh
```

## Configuration

Make directory `$XDG_CONFIG_HOME/betterlockscreen_rapid/` and write your own configuration file `betterlockscreen_rapid.conf` there.

You can use `betterlockscreen_rapid.conf` as a reference. More information can be found at [betterlockscreen][].

Note that `$XDG_CONFIG_HOME` defaults to `$HOME/.config/`.

In this particular fork, you can add 4 additional parameters to these config files:

* `before`: command, which is to be executed *before* locking the system
* `after`: command, which is to be executed *after* unlocking the system
* `radius`: default radius value
* `time`: default times value

Example config file:
```ìni
# /etc/betterlockscreen.conf or ~/.config/betterlockscreen.conf
# ... other settings ... #
before='razer-cli -b 0'     # Turn off RGB
after='razer-cli -a -b 100' # Turn on RGB
radius='10'                 # Set default radius
time='3'                    # Set default times
# ... other settings ... #
```

Any of these will be overriden by parameters, passed via the command line.

## Usage

```bash
betterlockscreen_rapid <radius> <times> <command>
```

- `radius` is the kernel size of the box filter.
- `times` is the number of times we filter the image.
- `command` is the command to be executed upon unlocking the system.

More information can be found at [i3lock-fancy-rapid][].

## Dependencies

- [i3lock-color][]
- [i3lock-fancy-rapid][]

[i3lock-color]: https://github.com/Raymo111/i3lock-color
[i3lock-fancy-rapid]: https://github.com/yvbbrjdr/i3lock-fancy-rapid
[betterlockscreen]: https://github.com/pavanjadhaw/betterlockscreen
