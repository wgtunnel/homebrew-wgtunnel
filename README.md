# homebrew-wgtunnel

Homebrew tap for [WG Tunnel](https://wgtunnel.com), an advanced, open-source client for
WireGuard and AmneziaWG.

## Install

```bash
brew tap wgtunnel/wgtunnel
brew trust wgtunnel/wgtunnel
brew install --cask wg-tunnel
```

## Update

The cask tracks the `wgtunnel/desktop` repo's latest GitHub release. It updates itself
automatically shortly after each release via a repository dispatch.

## Uninstall

Before uninstalling, use **Settings -> General -> Remove background service** in the app
itself, then:

```bash
brew uninstall --zap wg-tunnel
```

Skipping the in-app step first leaves the background service (a LaunchDaemon) running until
you reboot (macOS has no hook that automatically uninstalls the daemon when the app bundle is removed).
