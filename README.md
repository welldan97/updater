Updater
=======

Updater is here for making updates a little bit easier. Right now there are
quite a lot of different pieces needed to be babysitted and updated in different
ways and different sources, using different package managers. This wher updater
comes into play it helps updating using one command `updater update`, and that's
it. You can then run it every week or even automate further with i.e. launchd.

Updater is made for OS X, but I guess it can work with Linuxes too.

Supported updaters:

1. brew
2. brew cask
3. osx-software
4. oh-my-zsh
5. ~~node packages~~(coming soon)
6. ~~ruby gems~~(coming soon)
7. [~~emacs prelude~~][emacs-prelude](coming soon)

Installation
------------

### Homebrew

```bash
brew tap welldan97/updater
brew install updater
```

### Manual

```bash
git clone https://github.com/welldan97/updater.git
```

And then make sure that `updater` is in your `$PATH`. `updater.d` should be
in the same dir as `updater`, otherwhise you can specifay your own path by
setting `$UPDATER_PATH`.

Usage
-----

```bash
  $ updater list

Brew:
 ffmpeg
 fontconfig
 freetype
 imagemagick
 watchman
 youtube-dl
 zsh-completions

Brew Cask:
  dockertoolbox
  flash
  flux
  launchcontrol
  postgres
  vlc
  vox

Oh My ZSH:
  Needs update

OSX Software:
  OS X El Capitan Update-10.11.3
```

```bash
  $ updater update
```

`update` — Update everything

`list` — List available updates

`count` — Count available updates

`help` — Show help

Customization
-------------

You can have a look to [current updaters][updaters] available to implement your
own.


[updaters]: https://github.com/welldan97/updater/tree/master/updater.d
[emacs-prelude]: https://github.com/bbatsov/prelude
