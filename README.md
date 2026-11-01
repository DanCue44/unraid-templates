# Unraid templates

Community Applications templates for apps by DanCue44.

| App | What it does | Template | Support |
| --- | --- | --- | --- |
| [Talearr](https://github.com/DanCue44/Talearr) | Ebook and audiobook collection manager, a drop-in fork of Chaptarr | [talearr.xml](templates/talearr.xml) | [Forum](https://forums.unraid.net/topic/201142-support-dancue44-talearr/), [Issues](https://github.com/DanCue44/Talearr/issues) |
| [Allseerr](https://github.com/DanCue44/Allseerr) | Request manager for movies, series, music, books and audiobooks | [allseerr.xml](templates/allseerr.xml) | [Forum](https://forums.unraid.net/topic/200966-support-dancue44-allseerr/), [Issues](https://github.com/DanCue44/Allseerr/issues) |

## Allseerr install notes

- The container runs as UID 1000 and ignores PUID and PGID. Before the first start run:
  `mkdir -p /mnt/user/appdata/allseerr && chown -R 1000:1000 /mnt/user/appdata/allseerr`
- Coming from Seerr or Overseerr: stop it, copy its appdata folder to `/mnt/user/appdata/allseerr`, chown it as above, then start Allseerr. Keep the old folder as a backup.
- Docs: https://github.com/DanCue44/Allseerr/tree/main/docs

## Talearr install notes

- Coming from Chaptarr: stop Chaptarr and point Talearr's Appdata at Chaptarr's appdata folder (or a copy of it). Talearr reads the same config and database, so you can switch back the same way.
- Book data comes from Hardcover with a free personal API token (hardcover.app > Settings > API, then paste it in Talearr under Settings > Metadata). Without a token Talearr uses the Chaptarr metadata server.
- Keep downloads and the library on the same share and map one parent folder if you want hardlinks.
- Docs: https://github.com/DanCue44/Talearr#readme
