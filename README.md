# Iron Coffins

A turn-based artillery combat game for desktop. Take aim, account for
wind and gravity, and shell your opponents off a destructible landscape.
Made for hot-seat play — pass the keyboard.

> **Downloads-only repository.** Source for the game lives in a private
> repository; this repo hosts the built releases.
>
> **Game site:** <https://iron-coffins.github.io> — overview, full
> controls, store catalog, settings reference.

## Download

Grab the latest build for your platform from the
**[Releases page](https://github.com/iron-coffins/iron-coffins/releases/latest)**.

| Platform | Asset                       |
| -------- | --------------------------- |
| macOS    | `iron-coffins-macos.zip`    |
| Windows  | `iron-coffins-windows.zip`  |
| Linux    | `iron-coffins-linux.tar.gz` |

Builds are currently **unsigned**, so your operating system will warn
you the first time you launch them. See the platform notes below for
how to bypass the warning safely.

## Install & run

### macOS

1. Unzip the download, then drag **Iron Coffins** to `/Applications`.
2. First launch: right-click (or Control-click) the app → **Open** →
   **Open**.
3. After that, double-click launches normally.

If you double-click first, macOS will refuse with "cannot be opened
because the developer cannot be verified." The right-click → Open trick
adds an explicit override. Alternatively, after the blocked attempt go
to **System Settings → Privacy & Security**, scroll down, and click
**Open Anyway**.

### Windows

1. Unzip the archive somewhere stable (e.g. `C:\Games\IronCoffins`).
2. Launch `IronCoffins.exe`.

SmartScreen may flag the binary on first launch. Click **More info →
Run anyway** to proceed.

### Linux

```sh
tar -xzf iron-coffins-linux.tar.gz -C ~/Apps/iron-coffins
~/Apps/iron-coffins/iron-coffins
```

You may need to install runtime GTK and GStreamer packages on a minimal
distro:

```sh
sudo apt-get install libgtk-3-0 libgstreamer1.0-0 libgstreamer-plugins-base1.0-0
```

## How to play

* **Setup:** pick how many players (2–10), how many rounds, then
  configure each tank — human or AI, name, AI difficulty, tank
  silhouette (including the immobile bunker emplacement), and team color.
* **Each turn:** rotate your turret, dial in firing power, watch the
  wind indicator, and pick a weapon. Move left/right if you have fuel.
* **Each round:** survive, score damage, and earn cash to spend in the
  pre-round shop on better weapons, defenses, fuel, parachutes, and
  shields.
* **End of match:** scoring is tunable in Settings — basic kill+survive,
  damage-based standard, or greedy net-worth ranking.

## Controls

| Action             | Key(s)                         |
| ------------------ | ------------------------------ |
| Aim turret         | ← / →                          |
| Adjust power       | ↑ / ↓                          |
| Fine adjust        | Hold Shift + arrows            |
| Cycle weapon       | Tab / Shift+Tab (or `=` / `[`) |
| Select weapon slot | 1 – 9                          |
| Fire               | Space or Enter                 |
| Move tank          | A / D  (or `,` / `.`)          |

Shields are activated in the pre-round modal; batteries are used via
the in-turn HUD. All hotkeys are also surfaced as on-screen buttons.
For the full how-to-play walkthrough, see
<https://iron-coffins.github.io/play/>.

## System requirements

* **macOS:** 11 Big Sur or newer (Apple Silicon or Intel).
* **Windows:** 10 / 11, 64-bit.
* **Linux:** any modern distro with GTK 3 and GStreamer base plugins.

The game is lightweight — there's no GPU shader work beyond standard
Flutter/Flame rendering, so integrated graphics are plenty.

## License

The published binaries are distributed under the terms shown in each
release's notes. The source code is not currently published.
