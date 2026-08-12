# Luxus Videos — Thumbnails

Bildablage für die YouTube-Uploads der Luxus-Reihe. Öffentlich, damit
`youtubeThumbnailUrl` bei upload-post dauerhaft erreichbar bleibt (das Staging von
upload-post läuft nach 6 Stunden ab, `raw.githubusercontent.com` nicht).

Quelle je Video: `D:\Luxus Videos\<Ordner>\Thumbnail\final\` — dort liegt genau ein
finales Thumbnail, hier auf den Ordnernamen umbenannt.

| Video | Quelldatei | URL |
|---|---|---|
| 01 Teuerste Yacht | thumbnail_yacht_yt.jpg | https://raw.githubusercontent.com/evoldotv-ops/luxus-videos/main/01_teuerste_yacht.jpg |
| 02 Teuerster Privatjet | thumbnail_privatjet_yt.jpg | https://raw.githubusercontent.com/evoldotv-ops/luxus-videos/main/02_teuerster_privatjet.jpg |
| 03 Teuerste Autos | thumbnail_autos_yt.jpg | https://raw.githubusercontent.com/evoldotv-ops/luxus-videos/main/03_teuerste_autos.jpg |
| 04 Teuerste Häuser | thumbnail_haeuser_yt.jpg | https://raw.githubusercontent.com/evoldotv-ops/luxus-videos/main/04_teuerste_haeuser.jpg |
| 05 Teuerste Privatinseln | thumbnail_inseln_gen.jpg | https://raw.githubusercontent.com/evoldotv-ops/luxus-videos/main/05_teuerste_privatinseln.jpg |
| 06 Teuerste Uhren | thumbnail_uhren_set.webp | https://raw.githubusercontent.com/evoldotv-ops/luxus-videos/main/06_teuerste_uhren.jpg |

Alle unter 2 MB. 01–04 und 06 sind 1280×720, 05 liegt in 2048×1152 (YouTube skaliert
selbst herunter).

**Zwei Abweichungen gegenüber der Quelle:**
- 06 lag als `.webp` vor — die YouTube-Thumbnail-API nimmt nur JPEG/PNG, deshalb hier
  als JPG (ffmpeg `-q:v 2`, verlustarm neu kodiert).
- 05 ist die `_gen`-Fassung in 2048×1152, nicht wie die anderen eine `_yt`-Fassung.

Nach dem letzten Upload darf das Repo weg — YouTube hostet die Thumbnails dann selbst.
