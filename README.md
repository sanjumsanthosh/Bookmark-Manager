# Bookmark Manager

**Find the duplicates, see the folders, clean the mess.** A single-file browser tool for a Chrome
bookmark export — no install, no account, nothing uploaded.

```
main:/  →  https://sanjumsanthosh.github.io/Bookmark-Manager/
```

## Why

Chrome's bookmark manager tells you how many bookmarks you have. It doesn't tell you that you saved
the same article three times under three different titles, or that you have 400 bookmarks in one
flat folder.

Import the HTML export and this tool groups the damage:

| Duplicate kind | What it catches |
|---|---|
| **URL** | Exact same link saved twice |
| **Domain** | Many links from the same site — usually "I'll read it later" decay |
| **Title** | Same page saved under slightly different names |

## Use it

1. Open the page (or run it locally — it's one `index.html`).
2. Export bookmarks from Chrome: **Bookmarks → Bookmark manager → ⋮ → Export bookmarks**.
3. Drop the `.html` file in.
4. Walk the folder tree, review duplicates by group, and delete what you don't need.

Everything happens in the page. The file is parsed with the browser's own `DOMParser`; nothing is
sent anywhere and there is no backend.

## What it is not

- **Chrome-tested only.** It parses the standard Netscape bookmark export format, which other
  browsers also emit, but only Chrome was exercised.
- **It does not write back.** You get a clean list to act on; Chrome's own manager still does the
  deleting.
- **No sync, no storage.** Reload and it's empty.

## Run locally

```bash
git clone https://github.com/sanjumsanthosh/Bookmark-Manager
cd Bookmark-Manager
python3 -m http.server 8000    # or just open index.html
```

## Author

[@sanjumsanthosh](https://github.com/sanjumsanthosh)
