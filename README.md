# MyLyricSong

**A modern web-based lyric player and lyric page generator inspired by modern music streaming interfaces.**

MyLyricSong is a lightweight, browser-based tool for creating beautiful standalone music pages with **synchronized lyrics, audio playback, cover artwork, credits, metadata, and sharing support**.

It is designed with a visual experience inspired by modern music platforms such as Spotify, while remaining an independent project with its own implementation, branding, and codebase.

🌐 **Live Demo:** https://jproject-1.github.io/mylyricsong/

---

## ✨ Features

### 🎵 Audio Player

MyLyricSong allows you to create a complete standalone audio player from your browser.

Supported audio files include common browser-compatible formats such as:

* MP3
* WAV
* Other browser-supported audio formats

The generated player includes:

* Play / pause
* Current playback time
* Total duration
* Seek bar
* Skip backward 5 seconds
* Skip forward 5 seconds
* Automatic reset when playback ends
* Responsive mobile-friendly controls

The audio file can be embedded directly into the generated preview or packaged into the exported ZIP project.

---

### 📝 Synchronized Lyrics

MyLyricSong supports lyrics written in the **LRC format**.

Example:

```lrc
[00:05.00]This is the first lyric
[00:10.50]This is the second lyric
[00:15.00]This is another line
```

The generated player automatically:

1. Parses the LRC timestamps.
2. Detects the currently playing lyric.
3. Highlights the active lyric.
4. Automatically scrolls the lyrics container.
5. Keeps the lyrics synchronized with the audio.

The active lyric becomes visually emphasized while inactive lyrics remain subdued.

---

### 🖼️ Cover Artwork

You can upload cover artwork for your song.

Supported image formats depend on browser support, including common formats such as:

* JPG
* PNG
* WebP
* Other browser-supported image formats

The cover artwork is used in multiple places:

* Music player
* Background blur effect
* Open Graph metadata
* Browser icon
* Apple touch icon
* Generated music metadata

The player also creates a blurred version of the cover artwork as part of its visual background.

---

### 👤 Credits

Add multiple contributors to your music project.

Each credit contains:

* Role
* Name

For example:

```text
Artist       John Doe
Producer     Jane Doe
Composer     Alex Smith
Lyricist     Example Person
```

MyLyricSong can also automatically detect the main artist from roles such as:

* Artist
* Vocal
* Singer
* Main Artist

If no artist is detected, the author field can be used as a fallback.

---

### 🎨 Custom Theme Color

You can select a dominant theme color for your generated music page.

The selected color is used to influence the player interface and background atmosphere.

Example:

```text
Theme Color: #10B981
```

This makes it possible to create different visual identities for different songs.

---

### 🔍 SEO Metadata

MyLyricSong includes optional metadata configuration for generated pages.

You can specify:

* Author / Main Creator
* Meta Description
* Theme Color
* Distribution License

The generated HTML includes metadata such as:

* `<title>`
* Meta description
* Author
* Robots directive
* Theme color
* Copyright information
* Open Graph metadata
* Schema.org structured data

Generated pages use the `MusicRecording` Schema.org type.

This can help search engines better understand the generated music page.

---

### 👀 Live Preview

You can preview your generated music player directly inside MyLyricSong.

Click:

**Generate Preview**

The application generates the player HTML and displays it inside an embedded preview window.

This allows you to verify:

* Cover artwork
* Song title
* Artist
* Audio controls
* Lyrics synchronization
* Credits
* Theme
* Overall layout

before exporting your project.

---

### 📦 JSON Export

MyLyricSong can export your project information as a JSON file.

The exported data can contain:

```json
{
  "title": "Example Song",
  "artist": "Example Artist",
  "audioData": {},
  "coverData": {},
  "lyrics": "[00:05.00]Example lyric",
  "credits": [],
  "seo": {}
}
```

This can be useful for:

* Backups
* Data storage
* Custom integrations
* Future development
* Reusing song information

---

### 🗜️ ZIP Export

MyLyricSong can generate a complete standalone ZIP package.

The exported project follows a structure similar to:

```text
Example_Song.zip
│
├── index.html
│
└── source/
    ├── audio.mp3
    └── cover.jpg
```

The generated `index.html` references the local files inside the `source` directory.

This makes the exported player suitable for:

* Static hosting
* Personal websites
* GitHub Pages
* Local playback
* Web projects
* Sharing as a standalone music page

No server-side backend is required for the generated player.

---

## 🎧 Generated Player

The generated music page is designed as a standalone experience.

It contains:

```text
┌──────────────────────────────┐
│          NOW PLAYING         │
│                              │
│        Album Artwork         │
│                              │
│     Song Title               │
│     Artist                  │
│                              │
│  0:00 ─────────────── 3:45   │
│                              │
│     ◀     ▶     ▶            │
└──────────────────────────────┘

Lyrics

First lyric line

Second lyric line

Currently playing lyric

Next lyric line


Credits

Artist             Example Artist
Producer            Example Producer
License             ...
```

The generated interface is responsive and designed primarily around a modern mobile music-player experience.

---

## 🛠️ How to Use

### 1. Open MyLyricSong

Visit:

https://jproject-1.github.io/mylyricsong/

---

### 2. Enter Song Information

Enter the song title.

Example:

```text
Song Title:
My Example Song
```

---

### 3. Upload Audio

Upload your audio file.

Example:

```text
my-song.mp3
```

Audio is required to generate the preview and ZIP package.

---

### 4. Upload Cover Artwork

Upload your cover image.

Example:

```text
cover.jpg
```

If no cover is provided, the generated player uses a default placeholder.

---

### 5. Add Lyrics

Paste your synchronized LRC lyrics.

Example:

```lrc
[00:00.00]Intro
[00:05.20]This is the first line
[00:09.80]This is the second line
[00:14.30]This is the third line
```

Make sure the timestamps correspond to the audio.

---

### 6. Add Credits

Add contributors using the **Credits** section.

For example:

```text
Role: Artist
Name: John Doe

Role: Producer
Name: Jane Doe

Role: Composer
Name: Alex Smith
```

You can add or remove credit entries as needed.

---

### 7. Configure SEO and Distribution Information

Optional advanced settings include:

```text
Author / Main Creator
Meta Description
Dominant Theme Color
Distribution License
```

These settings are included in the generated player metadata.

---

### 8. Generate Preview

Click:

**Generate Preview**

The player will appear in the Live Output Preview section.

---

### 9. Export Your Project

You have two export options.

#### Download JSON

Click:

**Download JSON**

This exports the current MyLyricSong project data.

#### Download ZIP

Click:

**Download ZIP**

This creates a complete standalone website package containing:

```text
index.html
source/audio.*
source/cover.*
```

You can then extract the ZIP and upload the files to a static web host.

---

## 📋 LRC Format

MyLyricSong uses timestamp-based LRC lyrics.

Basic syntax:

```lrc
[mm:ss.xx]Lyric text
```

Example:

```lrc
[00:00.00]Welcome to the song
[00:04.50]This is the first verse
[00:09.20]The lyrics follow the music
[00:14.80]And continue automatically
```

### Timestamp Format

The timestamp consists of:

```text
[minutes:seconds.centiseconds]
```

For example:

```text
[01:25.50]
```

means:

```text
1 minute
25.50 seconds
```

MyLyricSong automatically sorts parsed lyric lines by their timestamps.

---

## 💻 Technology

MyLyricSong is designed as a client-side web application.

### Core Technologies

* HTML5
* CSS3
* Vanilla JavaScript
* Tailwind CSS
* Font Awesome
* JSZip
* Web Audio / HTML5 Audio
* FileReader API
* Blob API
* Web Share API
* Schema.org structured data

The generated player itself does not require a JavaScript framework.

---

## 🔐 Privacy

MyLyricSong is designed to process your uploaded files directly in the browser.

Audio and image files are read using browser APIs and converted into data that can be used by the generated player.

The project does not require a dedicated backend server to generate the player.

However, once you export and publish a generated music page, **the files become accessible according to the hosting environment and distribution method you choose**.

Do not upload private or confidential audio, artwork, lyrics, or other materials unless you understand where the resulting files will be stored and published.

---

# ⚖️ Usage Rules

MyLyricSong is a tool for creating and packaging music-player pages. It does **not** grant ownership or distribution rights over the music, lyrics, artwork, recordings, or other materials you upload.

By using MyLyricSong, you are responsible for ensuring that you have the necessary rights or permissions for the content you use.

## You MAY

You may use MyLyricSong to:

* Create lyric pages for your own music.
* Create lyric pages for music you are authorized to distribute.
* Create personal music-player pages.
* Generate static HTML music players.
* Export JSON project data.
* Export ZIP packages.
* Host generated pages on compatible static hosting services.
* Modify generated HTML for your own projects.
* Customize the generated player for legitimate personal or commercial projects, subject to the rights of the content used.

---

## You MUST

You must:

* Respect copyright laws.
* Have appropriate permission to distribute uploaded music.
* Have appropriate permission to use uploaded lyrics.
* Have appropriate permission to use uploaded cover artwork.
* Respect the selected distribution license.
* Respect the rights of artists, composers, lyricists, producers, labels, and other copyright holders.
* Follow the terms of your hosting provider.
* Provide attribution when required by the selected license.

---

## You MUST NOT

You must not use MyLyricSong to:

* Distribute music without authorization.
* Redistribute copyrighted songs without permission.
* Claim someone else's music as your own.
* Remove required copyright notices or attribution.
* Use copyrighted lyrics without appropriate authorization.
* Use artwork without permission.
* Circumvent licensing restrictions.
* Create misleading pages that falsely identify the creator of a song.
* Use MyLyricSong to facilitate copyright infringement.
* Impersonate Spotify or another music service.
* Suggest that MyLyricSong is officially affiliated with Spotify.

---

# 🎵 Spotify Inspiration

MyLyricSong is **inspired by modern music streaming interfaces**, with Spotify being one of the primary visual references.

The project may use familiar concepts found in modern music players, such as:

* Album artwork
* Song title
* Artist information
* Playback controls
* Progress bars
* Lyrics
* Dark interface
* Music-focused layouts

However:

> **MyLyricSong is an independent project and is not affiliated with, endorsed by, sponsored by, or officially connected to Spotify.**

Spotify, its logo, branding, trademarks, and other intellectual property belong to their respective owners.

MyLyricSong does not attempt to reproduce Spotify's proprietary software or services.

The project uses its own implementation and branding.

---

# 📜 Content & Copyright Responsibility

MyLyricSong provides the **tool**, not the content.

For example, if you upload:

```text
song.mp3
cover.jpg
lyrics.lrc
```

you are responsible for ensuring that you are legally allowed to use and distribute all three files.

The developer of MyLyricSong does not automatically obtain ownership of uploaded content.

Similarly, providing a license option such as:

```text
CC BY 4.0
CC BY-NC 4.0
CC BY-ND 4.0
Public Domain / CC0
Standard Music License
All Rights Reserved
```

does not automatically make your content compatible with that license.

**Only select a license that you have the legal authority to apply to your content.**

---

# 🚀 Hosting a Generated Player

After exporting a ZIP package:

### 1. Extract the ZIP

```text
My_Song.zip
```

becomes:

```text
My_Song/
├── index.html
└── source/
    ├── audio.mp3
    └── cover.jpg
```

### 2. Upload the files

Upload the entire folder to your static hosting provider.

Examples include:

* GitHub Pages
* Netlify
* Cloudflare Pages
* Vercel
* Other compatible static hosting services

### 3. Open the generated page

Visit the URL provided by your hosting provider.

The player should load the local audio and cover files from the `source` directory.

---

# 📁 Recommended Project Structure

A generated MyLyricSong project can look like:

```text
my-song/
│
├── index.html
│
└── source/
    ├── audio.mp3
    └── cover.jpg
```

For larger projects, you can organize multiple generated players:

```text
music/
│
├── song-one/
│   ├── index.html
│   └── source/
│       ├── audio.mp3
│       └── cover.jpg
│
├── song-two/
│   ├── index.html
│   └── source/
│       ├── audio.mp3
│       └── cover.jpg
│
└── index.html
```

---

# 🌐 Live Demo

Try MyLyricSong online:

**https://jproject-1.github.io/mylyricsong/**

No installation is required.

---

# 🧩 Browser Compatibility

MyLyricSong relies on modern browser APIs including:

* HTML5 Audio
* FileReader
* Blob
* URL.createObjectURL
* iframe `srcdoc`
* Web Share API
* Clipboard API

For the best experience, use a modern version of:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

Some features, especially native sharing, may vary depending on browser and device support.

---

# 🐛 Known Considerations

### Audio Compatibility

The browser must support the uploaded audio format.

If a browser cannot decode a particular audio format, playback may not work.

### LRC Accuracy

Lyrics synchronization depends on the timestamps provided in the LRC file.

Incorrect timestamps will result in incorrectly synchronized lyrics.

### Large Audio Files

Because the application processes uploaded files in the browser, extremely large audio files may require significant browser memory.

For best results, use reasonably sized audio files.

### Generated File Size

When generating a ZIP package, the original audio and cover files are included in the package.

Large audio files therefore produce larger ZIP files.

---

# 🤝 Contributing

Contributions are welcome.

You can contribute by:

* Reporting bugs
* Suggesting improvements
* Improving UI/UX
* Improving lyric synchronization
* Improving browser compatibility
* Adding documentation
* Improving accessibility
* Optimizing performance

Before submitting major changes, it is recommended to discuss the proposed change first.

---

# 📄 License

MyLyricSong source code is released under the **MIT License**.

```text
MIT License

Copyright (c) 2026 JasonPw

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

# ⚠️ Important License Notice

The **MIT License applies to the MyLyricSong software/code**, not automatically to:

* Music
* Lyrics
* Album artwork
* Audio recordings
* Artist names
* Trademarks
* Logos
* Third-party libraries
* Third-party assets

Those materials may have their own copyright, licenses, or terms of use.

You are responsible for complying with the applicable rights and licenses for any content you add to MyLyricSong.

---

# 🙏 Credits

**MyLyricSong**

Created by:

**JASONPW & YCYLSTUDIO**

Inspired by modern music-player experiences and streaming platforms.

Special thanks to the open-source community and the developers of the web technologies and libraries that make this project possible.

---

# 📌 Disclaimer

MyLyricSong is an independent project.

It is **not affiliated with Spotify** and does not represent an official Spotify product.

Spotify and related trademarks are property of their respective owners.

MyLyricSong is provided as a tool for creating standalone music and lyric pages. Users are solely responsible for the legality of the content they upload, generate, publish, and distribute.

---

## ⭐ Support the Project

If you find MyLyricSong useful:

* ⭐ Star the repository
* 🐛 Report bugs
* 💡 Suggest features
* 🔧 Contribute improvements
* 📢 Share the project with other developers

---

**MyLyricSong — Create. Sync. Play. Share.**
