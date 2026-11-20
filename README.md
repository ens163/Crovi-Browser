# CROVI Browser

A fast, native-feeling Windows browser built with Tauri 2, Rust and WebView2.
The interface is a single hand-written HTML file (no framework, no bundler) and
every browser feature is implemented end to end, not mocked.

## Features

- **Tabs** — create, close, reopen (Ctrl+Shift+T), pin / unpin, drag to reorder
  (pinned tabs stay grouped first), right-click actions (duplicate, copy link,
  reload, close others / close to the right), per-tab zoom, loading state,
  favicons and live title updates. Pinned tabs render as compact favicon chips
  and are protected from close-others, close-right and GX bulk cleanup.
- **Quick tab switcher** — Ctrl+Shift+A opens a keyboard-driven palette that
  searches open tabs and recently closed ones; arrows to move, Enter to switch.
- **Split view** — show two web pages side by side from any tab's context menu;
  panes resize with the window and closing either tab ends the split.
- **Extensions** — built-in installable add-ons from the sidebar: an ad & tracker
  blocker (hides ad slots, strips tracking parameters, blocks popups) and a
  focus mode that declutters articles; installed set persists across restarts.
- **Recently closed** — the last 25 closed tabs are restored on restart, listed
  on the History page with one-click restore, and reachable from the omnibox.
- **Omnibox** — URL detection, five search engines, live suggestions from
  bookmarks and history, plus "switch to open tab" and "reopen closed tab"
  entries; keyboard navigation, security indicator.
- **Bookmarks** — star toggle, bookmarks bar, full manager with search, inline
  edit and delete.
- **History** — capped at 8,000 entries, search, delete one / clear all,
  grouped by day.
- **Downloads** — real WebView2 downloads, suggested filenames from
  `Content-Disposition`, unique paths, open / reveal / remove, private-window
  downloads are memory-only. Completion is tracked by destination path, so
  redirects and concurrent downloads do not leave stale statuses.
- **Private windows** — incognito webviews, separate download list, nothing
  written to history or the session file.
- **Workspaces** — save the current tab set under a name from the sidebar and
  switch back to it later; saved locally, update/delete per workspace, pinned
  tabs are left untouched and replaced tabs go to the recently-closed stack.
- **Themes and accents** — GX-style dark console, system / light / dark, five
  neon accent palettes (Crimson, Ultraviolet, Ion, Ember, Toxic), reduced
  motion support, and a force-dark switch that recolors light websites.
- **Wallpapers** — four original voxel-art landscapes for the new tab page
  (Forest Dawn, Aurora Peaks, Sky Islands, Crystal Depths), selectable from
  Settings → Appearance, with a readable glass overlay and a "None" option.
- **GX Control** — sidebar tool rail plus a live performance panel with real
  Win32 CPU and memory readings, an open-tab switcher, one-click cleanup for
  inactive tabs (pinned tabs are kept), and a CC0 ambient sound player with
  play / pause, volume and a live equalizer.
- **Settings** — search engine, homepage, bookmarks bar, session restore,
  compact tabs, new-tab focus, default zoom, data clearing.
- **Shortcuts** — Chrome-compatible set (see Settings → Keyboard shortcuts),
  including a page-focus bridge so shortcuts keep working inside web pages.
