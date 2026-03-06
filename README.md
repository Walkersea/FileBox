# 📦 FileBox

A fully offline, browser-based file storage app. Upload, preview, and manage files entirely in your browser — no server, no account, no internet required after the first load.

## Features

- **IndexedDB storage** — files persist across sessions with no practical size limit (limited only by your disk)
- **Upload files or entire folders** — drag & drop anywhere on the page, or use the Upload / Folder buttons
- **In-browser preview** — images, video, audio, PDFs, and text/code files all open inline
- **Download files** back to your PC at any time
- **Export as `.sus`** — bundles all your files into a single portable file
- **Import `.sus`** — restore your files on any device; duplicate files are skipped automatically
- **6 themes** — Dark, Light, Rose, Ocean, Amber, Slate (persists across sessions)
- **Filter by type** — All, Images, Video, Audio, Docs, Other
- **Sort** by date added, name, or size
- **Grid and list view**
- **Search** files by name

## Usage

Just open `filebox.html` in any modern browser. No build step, no dependencies, no server.

```
open filebox.html
```

## The `.sus` Format

`.sus` is a self-contained JSON bundle that stores all your files as base64. Use it to:

- Back up your FileBox library
- Transfer files between devices or browsers
- Archive a snapshot before clearing storage

To export: click **Export .sus** in the topbar.  
To import: click **Import .sus** and select your bundle file. Existing files won't be duplicated.

## File Preview Support

| Type | Preview |
|------|---------|
| Images (jpg, png, gif, webp, svg, avif…) | ✅ Inline |
| Video (mp4, webm, mov…) | ✅ Native player |
| Audio (mp3, wav, ogg, flac, m4a…) | ✅ Native player |
| PDF | ✅ Embedded viewer |
| Text / Code / JSON / CSV / Markdown | ✅ Raw text |
| Everything else | ⬇️ Download to open |

## Storage

FileBox uses **IndexedDB**, which means:

- Storage is limited by your browser's quota (typically gigabytes, not megabytes)
- Files are scoped to the origin — each browser/device has its own separate storage
- Clearing browser site data will erase your files — use **Export .sus** to back up first

## Browser Support

Works in all modern browsers that support IndexedDB and the File API: Chrome, Firefox, Edge, Safari, Brave, Arc.

> Folder upload (`webkitdirectory`) is supported in Chromium-based browsers and Firefox. Safari has partial support. Files inside uploaded folders preserve their relative path (e.g. `photos/trip/beach.jpg`).

## Privacy

Everything stays in your browser. No data is sent anywhere. No analytics, no tracking, no ads.
