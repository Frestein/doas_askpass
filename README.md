Doas AskPass
================

## Contents

-   [Usage](#usage)
-   [Dependencies](#dependencies)
-   [Installation](#installation)
-   [Uninstallation](#uninstallation)
-   [Configuration](#configuration)

Doas AskPass is a simple expect script that basically creates a
`sudo -A` equivalent for Doas. This allows you to graphically enter your
password.

## Usage

    doas_askpass <command>

## Dependencies

1.  Doas ([Jesse Smith](https://codeberg.org/thejessesmith/doas) & [OpenDoas](https://github.com/Duncaen/OpenDoas) supported)
2.  Expect

Dmenu-like menu is also recommended.

## Installation

``` sh
git clone https://codeberg.org/Frestein/doas_askpass
cd doas_askpass
doas make install
```

## Uninstallation

``` sh
cd doas_askpass
doas make uninstall
```

## Configuration

The graphical program that is expected by the script is set by the
`DOAS_ASKPASS` environment variable. Otherwise, the default is
`dmenu -P -p password`. You need the
[password](https://tools.suckless.org/dmenu/patches/password/) patch in
order for this to work. You can set the environment variable in
`~/.bashrc` or anywhere else that your shell is going to source. The
following is an example.

``` sh
DOAS_ASKPASS="dmenu -P -p password:"
```
