# BillFav

Favourites for the Unity **Project window**. Pin the assets and folders you open all day into pages,
and jump to them without digging through the tree.

## Features

- **Pages** of pinned assets and folders; drag anything from the Project window in, drag to reorder.
- **Switch pages** with the mouse wheel, number keys 1–9 or the arrow keys.
- **Overlay mode:** hold a modifier key over the Project window and the favourites appear on top of
  it; release to hide.
- Click to select/ping, double-click to open; folders open in the Project browser.
- Smooth fade and page-scroll animations (can be turned off).

## Install

Package Manager → **Add package from git URL…**

```text
https://github.com/billtruong003/BillFav.git#v1.0.0
```

Editor-only, Unity 6000.0+. Nothing is added to player builds.

## Use

- **Tools ▸ Bill ▸ BillFav Window** (Ctrl+Shift+F) opens the panel as a dockable window.
- Drag assets or folders onto it to pin them.
- With **Overlay mode** on, hold the activation key while the mouse is over the Project window.

## Settings

All under **Tools ▸ Bill ▸ BillFav**:

| Menu | |
|---|---|
| Shortcuts ▸ Scroll to change page / 1-9 keys to change page / Arrow keys navigation | input options |
| Animations ▸ Fade animations / Page scroll animation | turn animations off |
| Open when ▸ Holding Alt / Alt + Shift / Ctrl + Alt (Cmd + Alt on macOS) | overlay activation key |
| Overlay mode (Alt-key) | show favourites over the Project window |
| Disable BillFav | turn everything off without uninstalling |

## Where the data lives

Favourites are stored in a `BillFavData` asset. The first time it is needed BillFav looks for an
existing one anywhere in the project; if there is none it creates
`Assets/Settings/Editor/BillFavData.asset`. Commit it to share favourites with your team, or add it to
`.gitignore` to keep them personal. You can move the asset; BillFav finds it again.

## Notes

- The overlay hooks into Unity's internal `ProjectBrowser` through reflection. If a Unity update
  changes those internals, the overlay switches itself off and the window keeps working.
- Ctrl+Shift+F is also Unity's *Align With View*. Rebind either in **Edit ▸ Shortcuts**.

## License

MIT, see [LICENSE.md](LICENSE.md).
