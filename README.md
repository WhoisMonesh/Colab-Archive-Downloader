# Internet Archive Downloader

Download books, movies, software from archive.org to Google Drive.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/WhoisMonesh/Colab-Archive-Downloader/blob/main/Colab-Archive-Downloader.ipynb)

---

## Quick Start

1. **Open in Colab** (click badge above)
2. **Mount Drive** when prompted
3. **Set the IDENTIFIER** (the archive.org item ID, e.g. `"cookbook"`)
4. Optionally set FILE_FILTER to only download specific files
5. **Run all cells**

---

## Features

| Feature | Description |
|---|---|
| **Internet Archive** | Download any public item by identifier |
| **File Filter** | Only download files matching a string |
| **Live Progress** | Shows which file is downloading with size |
| **Recursive Zipping** | Preserves directory structure in zip |
| **Sync-safe** | Downloads locally, moves to Drive after |
| **Keep-Alive** | JavaScript prevents Colab timeout |

---

## Configuration

| Variable | Default | Description |
|---|---|---|
| `SAVE_PATH` | `/content/downloads/InternetArchiveDownloader/` | Local temp directory |
| `DRIVE_PATH` | `/content/drive/My Drive/InternetArchiveDownloader/` | Final Drive destination |
| `IDENTIFIER` | `""` | Archive.org item identifier |
| `FILE_FILTER` | `""` | Only download files containing this string (case-insensitive) |
| `KEEP_ALIVE` | `True` | Prevent Colab timeout |

### Finding the Identifier

The identifier is the part of the URL after `archive.org/details/`. For example:

| URL | Identifier |
|---|---|
| `https://archive.org/details/cookbook` | `cookbook` |
| `https://archive.org/details/msdos_art_of_war` | `msdos_art_of_war` |

---

## Technical Details

- Uses the [internetarchive](https://github.com/jjjake/internetarchive) Python library
- Downloads to `/content/downloads/` first, then `shutil.move` to Drive (avoids FUSE sync conflicts)
- Live HTML progress via `IPython.display` with `display_id`
- Recursive file handling via `os.walk` for proper zipping
- JavaScript keep-alive prevents Colab session timeout

---

## Fair Use & Legal Notice

This tool downloads content from the Internet Archive for **personal, offline use only**.

**You agree to:**
- Only download public domain or freely accessible items
- Comply with the Internet Archive's Terms of Service
- Respect copyright and licensing of each item

**You may NOT use this tool to:**
- Download copyrighted content without authorization
- Redistribute, re-upload, or share downloaded content
- Monetize downloaded content in any form

**Disclaimer:** The authors are not responsible for how you use this software. You assume all legal responsibility for the content you download. This tool is provided for educational purposes only.

---

## License

MIT
