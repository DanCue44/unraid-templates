# Unraid templates

Community Applications templates for apps by DanCue44.

| App | What it does | Template | Support |
| --- | --- | --- | --- |
| [AllSeerr](https://github.com/DanCue44/AllSeerr) | Request manager for movies, series, music, books and audiobooks | [allseerr.xml](templates/allseerr.xml) | [Issues](https://github.com/DanCue44/AllSeerr/issues) |

## AllSeerr install notes

- The container runs as UID 1000 and ignores PUID and PGID. Before the first start run:
  `mkdir -p /mnt/user/appdata/allseerr && chown -R 1000:1000 /mnt/user/appdata/allseerr`
- Coming from Seerr or Overseerr: stop it, copy its appdata folder to `/mnt/user/appdata/allseerr`, chown it as above, then start AllSeerr. Keep the old folder as a backup.
- Docs: https://github.com/DanCue44/AllSeerr/tree/main/docs
