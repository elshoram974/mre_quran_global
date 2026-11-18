# Mushafi: global files

Every media file the Mushafi app downloads, and its privacy policy, served with GitHub Pages from the
branch `global` of `elshoram974/mre_quran_global` (`AppConfig.mediaBase` in the app). New media goes here:

| Folder | What | Served at |
|---|---|---|
| `adhan/` | Adhan recordings downloaded on demand, cleaned by the app's `tool/audio/build_adhan_audio.py` | `https://elshoram974.github.io/mre_quran_global/adhan/<id>.m4a` |
| `privacy/` | The privacy policy (Arabic and English) | `https://elshoram974.github.io/mre_quran_global/privacy/` |
| `LINKS.md` | Every address the app downloads from | |

## Publishing

Commit and push the branch `global`; GitHub Pages (Settings, Pages: branch `global`, folder `/ (root)`)
publishes it within a minute or two.

## Changing a file

The app checks every download against its SHA-256 in `assets/adhan/voices.json`. A changed file needs the
app's catalogue rebuilt (`python3 tool/audio/build_adhan_audio.py ...`) and a new release of the app;
until then the app falls back to the original recording.
