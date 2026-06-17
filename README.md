# Internet Archive Downloader

Download books, movies, software from archive.org to Google Drive.

[![Open In Colab](https://colab.research.google.com/assets/github/WhoisMonesh/Colab-Archive-Downloader/blob/main/Colab-Archive-Downloader.ipynb)]

---

## Features
| Feature | Description |
|---|---|
| **Sync-safe** | Downloads to local temp, moves to Drive after |
| **Progress Bar** | Real-time HTML progress |
| **Keep-Alive** | Prevents Colab timeout |
| **Auto-Zip** | Zips multiple files with progress + download link |

## How to Use
1. Mount Google Drive
2. Install dependencies
3. Configure variables
4. Run download

### Configuration
| Variable | Default | Description |
|---|---|---|
| `SAVE_PATH` | `/content/downloads/.../` | Local temp dir |
| `DRIVE_PATH` | `/content/drive/My Drive/.../` | Final Drive destination |
| `IDENTIFIER` | `""` | Archive.org identifier |
| `FILE_FILTER` | `""` | Only download files containing this string |
| `KEEP_ALIVE` | `True` | Prevent Colab timeout |

### Features
- Download any item from archive.org by identifier
- File filter to download only specific formats
- Great for books, old software, public domain media

---

## Technical Details
- Downloads to `/content/downloads/` first, then moves to Drive
- Uses IPython.display HTML for live progress updates
- JavaScript keep-alive prevents session timeout

## Disclaimer
For legal use only.

## License
MIT
