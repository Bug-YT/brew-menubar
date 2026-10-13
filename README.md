# brew-menubar

> A macOS menu bar app for managing Homebrew: control services, check for updates and upgrade packages without opening a terminal.

brew-menubar shows the status of your [Homebrew services](https://github.com/Homebrew/homebrew-services) in the menu bar and lets you start, stop and restart them. Update and upgrade support is in development (see [Features](#features)).

<img src="docs/screenshot.png" alt="Screenshot" width="197">
<!-- TODO: replace with a new screenshot once the menu changes -->

> **Fork notice:** brew-menubar is a fork of [brew-services-menubar](https://github.com/andrewn/brew-services-menubar) by Andrew Nicolaou.

## Features

- [x] Show the status of all Homebrew services
- [x] Start and stop services
- [x] Restart a service (hold <kbd>Option</kbd>)
- [ ] Check for updates (`brew update`, `brew outdated`)
- [ ] Update and upgrade packages
- [ ] <!-- TODO: add further features as you commit to them -->

## Install

### Using Homebrew Cask

<!-- TODO: only keep this section once a cask/tap actually exists -->

```sh
brew install --cask brew-menubar
```

### Manually

Download the latest build from the [Releases](https://github.com/<your-user>/brew-menubar/releases) page.
<!-- TODO: insert your GitHub user/org -->

⚠️ You'll see a warning <cite>"brew-menubar" can't be opened because Apple cannot check it for malicious software</cite>. This happens because the app is not (yet) signed and notarized with a paid Apple developer account.

[More info about this warning](https://support.apple.com/en-gb/guide/mac-help/mchleab3a043/mac).

### Autostart

The app has no built-in autostart option yet. To launch it at login, open _System Settings_ -> _General_ -> _Login Items_ and add brew-menubar to the list.

## Usage

- Click a service name to start it
- Click a running service (indicated with a tick) to stop it
- Hold <kbd>Option</kbd> to restart a single service

## Configuration

By default, brew-menubar looks for Homebrew at `/usr/local/bin/brew` (Intel) and `/opt/homebrew/bin/brew` (Apple Silicon).
If this is not correct for your setup, you can customize it with:

```sh
defaults write <your.bundle.identifier> brewExecutable /usr/local/bin/brew
```
<!-- TODO: replace with your new bundle identifier -->

## License

<!-- TODO: clarify the license of the original project first, then state yours here -->

Icon is [Beer by Enemen from the Noun Project](https://thenounproject.com/search/?q=beer&i=783212).
