Updater
=======

![Updater](updater.png)

Updater is here for making updates a little bit easier. Right now there are
quite a lot of different pieces needed to be used and updated in different
ways and from different sources or using different package managers. This is
where updater comes into play it helps updating using one command
`updater update`, and that's it. Then you can run it every week or automate even
further with i.e. launchd.

Updater is made for OS X, but I guess it can work with Linuxes too.

Out of the box updaters:

1. brew
2. brew cask
3. osx-software
4. oh-my-zsh
5. [emacs prelude][emacs-prelude]
6. npm
5. ~~ruby gems~~(coming soon)

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
in the same directory as `updater`, otherwhise you can specify your own path by
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

---

Originally extracted from [welldan97/dotfiles][welldan97-dotfiles]

[emacs-prelude]: https://github.com/bbatsov/prelude
[updaters]: https://github.com/welldan97/updater/tree/master/updater.d
[welldan97-dotfiles]: https://github.com/welldan97/dotfiles
