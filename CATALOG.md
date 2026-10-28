# Photon Featured catalog (catalog.json)

The Featured tab in Photon Wallpapers reads one file from this repository: `catalog.json`.
The app saves it on the PC for 24 hours and uses the saved copy when there is no internet.

## The file

```json
{
  "version": 1,
  "name": "Photon Featured",
  "updated": "2026-10-27",
  "items": [
    {
      "id": "prism-dusk",
      "type": "image",
      "title": "Prism Dusk",
      "url": "https://raw.githubusercontent.com/JohnssNoww001/Photon-Wallpapers/main/featured/prism-dusk.jpg",
      "thumbnail": "https://raw.githubusercontent.com/JohnssNoww001/Photon-Wallpapers/main/featured/prism-dusk-thumb.jpg",
      "credit": "Photon Wallpapers",
      "creditUrl": "https://github.com/JohnssNoww001/Photon-Wallpapers",
      "license": "CC0 1.0",
      "licenseUrl": "https://creativecommons.org/publicdomain/zero/1.0/",
      "resolution": "3840x2160",
      "category": "Abstract",
      "tags": ["prism", "light", "rainbow", "dark"]
    }
  ]
}
```

## Top-level fields

| Field | Required | Meaning |
|---|---|---|
| `version` | no | Format version. Use `1`. |
| `name` | no | Title shown above the list. |
| `updated` | no | Date text shown above the list (for example `2026-10-27`). |
| `items` | **yes** | The list of wallpapers (can be empty). |

## Each item

| Field | Required | Meaning |
|---|---|---|
| `id` | **yes** | Short unique name (letters, numbers, `-`, `_`, `.`). Never change it after publishing (favorites use it). |
| `title` | **yes** | Name shown on the card. |
| `url` | **yes** | The full file. Must start with `https://`. Images: jpg, png, bmp. Videos: mp4 or webm. |
| `type` | no | `"image"` (default) or `"video"` (live wallpaper). |
| `thumbnail` | recommended | Small picture for the card (about 640 px wide). Must be `https://`. Images fall back to `url` if missing. |
| `preview` | no | Videos only: a short small clip (https) for the hover preview. |
| `credit` | recommended | Creator's name, shown on the card. |
| `creditUrl` | no | Link to the creator (https). Opens from the preview window. |
| `license` | recommended | Short license label shown on the card (for example `CC0 1.0`, `CC BY 4.0`). |
| `licenseUrl` | no | Link to the license text (https). |
| `resolution` | no | Text such as `3840x2160`. |
| `category` | no | One word for the filter buttons (for example `Nature`). |
| `tags` | no | Words used by the search box. |

Items with a missing `id`, `title` or a non-https `url` are skipped by the app.

## Adding a wallpaper (baby steps)

1. Put the picture in the `featured` folder of the repository, plus a small thumbnail.
2. Add a new block to `items` in `catalog.json`. Copy an old one and change it. Keep a comma between blocks.
3. Change `updated`.
4. Commit. The app picks it up within 24 hours, or right away when someone presses Refresh.

## Rules for what to add

Only add wallpapers you made yourself, or that have a license which allows sharing (for example CC0, or a CC license with the credit shown). Always fill in `credit` and `license`.

## Big videos

GitHub files in the repository are limited in size. For large live wallpapers, upload the video as a file on a GitHub Release and use that download link as `url`.
