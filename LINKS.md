# Every address Mushafi downloads from

What the app fetches from the internet, and from where. Anything here can be
copied into this repository and served from it instead (the app checks every
file against its SHA-256, so a copy must be the same bytes).

## Adhan voices and the dua after the adhan (on demand: a tap on listen or download)

The app asks this repository first (`https://elshoram974.github.io/mre_quran_global/adhan/<id>.m4a`,
the cleaned files in `adhan/`), and the original below if that fails.

| Voice | Original | Here |
|---|---|---|
| `egypt_harak` | https://archive.org/download/adhan-from-egypt-abdulnasser-harak/Adhan%20from%20Egypt%20Abdulnasser%20Harak.mp3 | `adhan/egypt_harak.m4a` (cleaned) |
| `mishary_alafasy` | https://archive.org/download/VeryBeautifulAdhaanByMisharyAlAfasy/Very%20Beautiful%20Adhaan%20by%20Mishary%20Al-Afasy.mp3 | `adhan/mishary_alafasy.m4a` (cleaned) |
| `makkah_ali_mullah_fajr` | https://archive.org/download/MakkahFajrAdhan6913SheikhAliMullah/Makkah%20Fajr%20Adhan%206-9-13%20Sheikh%20Ali%20Mullah.mp3 | `adhan/makkah_ali_mullah_fajr.m4a` (cleaned) |
| `mansoor_zahrani_fajr` | https://raw.githubusercontent.com/abodehq/Athan-MP3/cf1a9dd4f1e5e10009439099c5af74479ad332c0/Sounds/Athan%20Mansoor%20Az-Zahrani.mp3 | `adhan/mansoor_zahrani_fajr.m4a` (cleaned) |
| `malek_chebae_fajr` | https://raw.githubusercontent.com/abodehq/Athan-MP3/cf1a9dd4f1e5e10009439099c5af74479ad332c0/Sounds/Athan%20Al-fajer%20-%20Malek%20chebae.mp3 | `adhan/malek_chebae_fajr.m4a` (cleaned) |
| `dua_after_adhan_shaarawy` (the dua after the adhan) | https://archive.org/download/AD3YA---SHEKH---METOLLYAL---SHA3RAWY---MP3---Qass--nabwy--MP3/1.MP3 | `adhan/dua_after_adhan_shaarawy.m4a` (cleaned) |

The bundled voices (Nasser Al-Qatami's adhan, the default; Mishary Alafasy's Fajr adhan and dua) ship inside
the app; their originals are listed in the app's `tool/audio/adhan_sources.json`.

## Printed Mushaf pages (on demand: a page opened, or the whole Mushaf downloaded)

From the quran-ws/quran-svg project, release v1.1.1 (artwork: King Fahd Complex; ayah positions: Quran.ws).
Not copied here: about 600 MB for the five readings. To serve them from here, put each archive under
`mushaf/<edition>/` with the same name, and change `base` and the archive `url`s in the app's
`assets/quran/svg/<edition>_kfqc_manifest.json` (the SHA-256 stay).

| Reading | Address | Size |
|---|---|---|
| hafs | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/hafs-kfqc-svg.zip | 121.6 MB |
| hafs | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/hafs-kfqc-json.zip | 0.5 MB |
| hafs (each page) | `https://cdn.quran.ws/svg/pages/v1.1.1/hafs-kfqc/NNN.svg` and `NNN.json`, NNN = 001…604 | |
| warsh | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/warsh-kfqc-svg.zip | 131.8 MB |
| warsh | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/warsh-kfqc-json.zip | 0.5 MB |
| warsh (each page) | `https://cdn.quran.ws/svg/pages/v1.1.1/warsh-kfqc/NNN.svg` and `NNN.json`, NNN = 001…604 | |
| qalon | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/qalon-kfqc-svg.zip | 123.7 MB |
| qalon | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/qalon-kfqc-json.zip | 0.5 MB |
| qalon (each page) | `https://cdn.quran.ws/svg/pages/v1.1.1/qalon-kfqc/NNN.svg` and `NNN.json`, NNN = 001…604 | |
| douri | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/douri-kfqc-svg.zip | 113.8 MB |
| douri | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/douri-kfqc-json.zip | 0.5 MB |
| douri (each page) | `https://cdn.quran.ws/svg/pages/v1.1.1/douri-kfqc/NNN.svg` and `NNN.json`, NNN = 001…604 | |
| shubah | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/shubah-kfqc-svg.zip | 117.6 MB |
| shubah | https://github.com/quran-ws/quran-svg/releases/download/v1.1.1/shubah-kfqc-json.zip | 0.5 MB |
| shubah (each page) | `https://cdn.quran.ws/svg/pages/v1.1.1/shubah-kfqc/NNN.svg` and `NNN.json`, NNN = 001…604 | |

## Not downloads of files

| What | Address | Why not here |
|---|---|---|
| Map, when choosing a place | Google Maps SDK | A live service |
| Finding a city by name | The phone's own geocoder (Google on Android, Apple on iOS) | A live service |
| Crash reports (sent, not fetched) | Firebase Crashlytics | A live service |
| Privacy policy | `privacy/index.html` here: https://elshoram974.github.io/mre_quran_global/privacy/ | Already here |
| Contact | WhatsApp https://wa.me/201553668845, email riyadm2001@gmail.com | Links, not downloads |
