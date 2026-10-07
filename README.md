# 🎵 MyLyricSong

**A modern, browser-based lyric player and standalone music-page generator.**

MyLyricSong is a lightweight web application for creating beautiful standalone music pages with:

- 🎵 Audio playback
- 📝 Synchronized LRC lyrics
- 🖼️ Cover artwork
- 👤 Artist and contributor credits
- 🎨 Custom theme colors
- 🔍 SEO metadata
- 📱 Responsive music-player UI
- 📦 JSON project export
- 🗜️ Standalone ZIP export
- 🔗 Web Share support

It is designed around a modern music-streaming experience while remaining an **independent project with its own implementation, branding, and codebase**.

> **No backend is required.**  
> Your files are processed directly in the browser.

🌐 **Live Demo:**  
https://jproject-1.github.io/mylyricsong/

---

# ✨ Features

## 🎵 Audio Player

MyLyricSong generates a complete standalone HTML music player directly in your browser.

Supported formats depend on the browser, including common formats such as:

- MP3
- WAV
- Other browser-supported audio formats

The generated player includes:

- ▶️ Play / pause
- ⏱️ Current playback time
- ⏱️ Total duration
- 🎚️ Seek bar
- ⏪ Skip backward 5 seconds
- ⏩ Skip forward 5 seconds
- 🔄 Automatic player reset when playback ends
- 📱 Responsive mobile-friendly controls

When exporting a ZIP package, the original audio file is placed inside the generated `source/` directory.

Example:

```text
source/
└── audio.mp3
```

---

# 📝 Synchronized Lyrics

MyLyricSong supports timestamp-based **LRC lyrics**.

Example:

```lrc
[00:05.00]This is the first lyric
[00:10.50]This is the second lyric
[00:15.00]This is another line
```

The generated player automatically:

1. Parses the LRC timestamps.
2. Sorts lyrics by timestamp.
3. Detects the currently playing lyric.
4. Highlights the active lyric.
5. Automatically scrolls the lyric container.
6. Synchronizes lyrics with audio playback.

The currently active lyric is displayed more prominently while inactive lines remain visually subdued.

---

# 🖼️ Cover Artwork

You can upload a cover image for your song.

Common browser-supported formats include:

- JPG / JPEG
- PNG
- WebP
- Other browser-supported image formats

The cover artwork can be used as:

- 🎨 Main player artwork
- 🌫️ Blurred background
- 🌐 Open Graph image
- 🌐 Browser icon
- 🍎 Apple touch icon
- 🎵 Generated music metadata

If no artwork is provided, MyLyricSong uses a default placeholder.

---

# 👤 Credits

Add multiple contributors to your music project.

Each credit contains:

```text
Role
Name
```

Example:

```text
Artist       John Doe
Producer     Jane Doe
Composer     Alex Smith
Lyricist     Example Person
```

MyLyricSong can automatically detect the main artist from common roles such as:

- Artist
- Vocal
- Singer
- Main Artist

If no artist role is detected, the **Author / Main Creator** field can be used as a fallback.

---

# 🎨 Custom Theme Color

Choose a dominant theme color for the generated music page.

Example:

```text
Theme Color: #10B981
```

The selected color influences the generated player background and overall visual atmosphere.

This allows different songs to have different visual identities.

---

# 🔍 SEO & Metadata

MyLyricSong provides optional metadata configuration for generated music pages.

Available settings include:

- Author / Main Creator
- Meta Description
- Dominant Theme Color
- Distribution License

Generated pages can contain metadata such as:

```html
<title>
<meta name="description">
<meta name="author">
<meta name="robots">
<meta name="theme-color">
<meta name="copyright">
```

Open Graph metadata is also generated for supported sharing platforms.

The generated player additionally includes Schema.org structured data using:

```text
MusicRecording
```

This helps search engines better understand the content of the generated music page.

> SEO metadata does not guarantee search-engine indexing or ranking.

---

# 👀 Live Preview

MyLyricSong includes a built-in live preview system.

After entering your information, click:

**Generate Preview**

The application generates the standalone player and displays it inside the preview area.

You can check:

- Cover artwork
- Song title
- Artist
- Audio playback
- Progress bar
- Lyrics synchronization
- Credits
- Theme color
- Overall layout

before exporting the project.

The preview is generated locally using an embedded HTML document.

---

# 📦 JSON Export

MyLyricSong can export your current project data as a JSON file.

Example:

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

JSON export can be useful for:

- 💾 Backups
- 🗃️ Data storage
- 🔧 Custom integrations
- 🧪 Development
- ♻️ Reusing project information
- 📦 Creating your own workflow around MyLyricSong

The JSON file is intended as **project data**, not as the final standalone music page.

---

# 🗜️ ZIP Export

MyLyricSong can generate a complete standalone website package.

Example:

```text
Example_Song.zip
│
├── index.html
│
└── source/
    ├── audio.mp3
    └── cover.jpg
```

The generated `index.html` references the local files inside the `source/` directory.

The resulting project can be used with compatible static hosting services.

Examples:

- GitHub Pages
- Netlify
- Cloudflare Pages
- Vercel
- Other static hosting providers

No PHP, Node.js, database, or server-side backend is required for the generated player.

---

# 🎧 Generated Player

The generated page provides a standalone music experience.

Its interface contains:

```text
┌──────────────────────────────┐
│          NOW PLAYING         │
│                              │
│        Album Artwork         │
│                              │
│        Song Title            │
│        Artist                │
│                              │
│  0:00 ─────────────── 3:45   │
│                              │
│       ◀     ▶     ▶          │
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

The generated player is designed primarily around a modern mobile music-player experience while remaining responsive on larger screens.

---

# 🚀 Quick Start

## 1. Open MyLyricSong

You can use the live version directly in your browser:

**Live Demo**

https://jproject-1.github.io/mylyricsong/

No installation is required.

---

## 2. Enter Your Song Title

Enter the title of your song.

Example:

```text
Song Title:
My Example Song
```

---

## 3. Upload Audio

Upload your audio file.

Example:

```text
my-song.mp3
```

An audio file is required for:

- Preview generation
- ZIP export

The browser must support the selected audio format.

---

## 4. Upload Cover Artwork

Upload your cover image.

Example:

```text
cover.jpg
```

If no cover is provided, MyLyricSong uses a default placeholder.

---

## 5. Add Lyrics

Paste your synchronized LRC lyrics.

Example:

```lrc
[00:00.00]Intro
[00:05.20]This is the first line
[00:09.80]This is the second line
[00:14.30]This is the third line
```

Make sure the timestamps match the audio.

---

## 6. Add Credits

Use the **Credits** section to add contributors.

Example:

```text
Role: Artist
Name: John Doe

Role: Producer
Name: Jane Doe

Role: Composer
Name: Alex Smith
```

You can add or remove contributors as needed.

---

## 7. Configure Advanced Settings

Optional settings include:

```text
Author / Main Creator
Meta Description
Dominant Theme Color
Distribution License
```

These values are included in the generated player's metadata.

---

## 8. Generate Preview

Click:

**Generate Preview**

The generated music player will appear inside the **Live Output Preview** area.

---

## 9. Export Your Project

MyLyricSong provides two export options.

### Download JSON

Click:

**Download JSON**

This downloads the current project configuration and data.

### Download ZIP

Click:

**Download ZIP**

This generates a standalone website package:

```text
index.html
source/
├── audio.*
└── cover.*
```

Extract the ZIP and upload the files to a compatible static hosting provider.

---

# 📋 LRC Format

MyLyricSong uses timestamp-based LRC lyrics.

## Basic Syntax

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

## Timestamp Format

A timestamp follows this format:

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

MyLyricSong automatically sorts parsed lyric lines by timestamp.

### Important

Lyrics synchronization depends on the timestamps you provide.

Incorrect timestamps will result in incorrectly synchronized lyrics.

---

# 🧩 Download Without Git Clone

MyLyricSong is designed to be easy to obtain without requiring Git.

You **do not need to run**:

```bash
git clone
```

If you only want to use or distribute a released version, download the project from the repository's **GitHub Releases** section.

Typical workflow:

```text
GitHub Releases
      │
      ▼
Download ZIP
      │
      ▼
Extract files
      │
      ▼
Open MyLyricSong
      │
      ▼
Create your music page
```

This makes the project accessible to users who do not use Git or GitHub's command-line tools.

> Releases are intended for convenient distribution of ready-to-use project versions.

If you are developing or modifying the source code, you can instead download the repository source or use Git according to your preferred workflow.

---

# 🛠️ Technology

MyLyricSong is a client-side web application.

## Core Technologies

- HTML5
- CSS3
- Vanilla JavaScript
- Tailwind CSS
- Font Awesome
- JSZip
- HTML5 Audio API
- FileReader API
- Blob API
- URL / Object URLs
- Web Share API
- Clipboard API
- `iframe srcdoc`
- Schema.org structured data

The generated music player itself does not require a JavaScript framework.

---

# 🔒 Privacy

MyLyricSong is designed to process uploaded files directly inside your browser.

Audio and image files are read using browser APIs such as:

```text
FileReader
Blob
URL.createObjectURL
```

The application does not require a dedicated backend server to generate the player.

### Important

When you export a project, your uploaded files can become part of the generated output.

For example:

```text
song.mp3
cover.jpg
lyrics
```

may be included in the generated ZIP package or embedded into generated data.

Once you publish the generated files online, their availability depends on the hosting service and distribution method you choose.

**Do not upload private, confidential, or sensitive content unless you understand how the resulting files will be stored and distributed.**

---

# ⚠️ Content & Copyright Responsibility

MyLyricSong is a **creation and packaging tool**.

It does not grant you ownership, copyright, licensing rights, or distribution rights to any content you upload.

For example, if you upload:

```text
song.mp3
cover.jpg
lyrics.lrc
```

you are responsible for ensuring that you have the necessary rights or permissions to use and distribute all three.

This includes rights relating to:

- Music
- Audio recordings
- Lyrics
- Artwork
- Artist names
- Composer credits
- Producer credits
- Trademarks
- Logos
- Other third-party material

The MyLyricSong developers do not automatically obtain ownership of content you upload.

---

# ⚖️ Usage Rules

MyLyricSong is provided as a tool for creating standalone music and lyric pages.

## ✅ You MAY

You may use MyLyricSong to:

- Create lyric pages for your own music.
- Create pages for music you are authorized to distribute.
- Create personal music-player pages.
- Generate standalone HTML players.
- Export JSON project data.
- Export ZIP packages.
- Host generated pages on compatible hosting services.
- Modify generated HTML.
- Customize the generated player.
- Use the generated player in legitimate personal projects.
- Use the generated player in legitimate commercial projects, provided that you have the necessary rights to the content.

---

## 📌 You MUST

You must:

- Respect applicable copyright laws.
- Have permission to distribute uploaded music.
- Have permission to use uploaded lyrics.
- Have permission to use uploaded artwork.
- Respect the license you select for your content.
- Respect the rights of artists, composers, lyricists, producers, labels, and other rights holders.
- Follow the terms of your hosting provider.
- Provide attribution when required by a license.

---

## ❌ You MUST NOT

You must not use MyLyricSong to:

- Distribute music without authorization.
- Redistribute copyrighted music without permission.
- Claim someone else's music as your own.
- Use copyrighted lyrics without appropriate authorization.
- Use artwork without permission.
- Remove legally required attribution.
- Circumvent licensing restrictions.
- Create misleading copyright or ownership information.
- Falsely identify yourself as the creator of someone else's work.
- Facilitate copyright infringement.
- Impersonate Spotify or another music service.
- Suggest that MyLyricSong is officially affiliated with Spotify.

---

# 📜 Distribution Licenses

MyLyricSong provides several license choices for the **content you generate**, including options such as:

```text
All Rights Reserved
CC BY 4.0
CC BY-NC 4.0
CC BY-ND 4.0
Public Domain / CC0
Standard Music License
```

Selecting a license in MyLyricSong **does not automatically grant that license to your content**.

For example, selecting:

```text
CC BY 4.0
```

does not make copyrighted music or lyrics Creative Commons licensed.

You must have the legal authority to apply the selected license.

> **Only select a license that you are legally authorized to use for the content you are distributing.**

---

# 🎵 Spotify Inspiration & Trademark Notice

MyLyricSong is inspired by modern music-streaming interfaces, with Spotify being one of its visual references.

The project uses familiar concepts found in modern music players, such as:

- Album artwork
- Song titles
- Artist information
- Playback controls
- Progress bars
- Lyrics
- Dark interfaces
- Music-focused layouts

However:

> **MyLyricSong is an independent project and is not affiliated with, endorsed by, sponsored by, or officially connected to Spotify.**

Spotify, its logo, trademarks, branding, and related intellectual property belong to their respective owners.

MyLyricSong does not attempt to reproduce Spotify's proprietary software, services, or backend infrastructure.

The project uses its own implementation and branding.

---

# 🌐 Hosting a Generated Player

After downloading a ZIP package, extract it.

## 1. Extract the ZIP

Example:

```text
My_Song.zip
```

After extraction:

```text
My_Song/
├── index.html
└── source/
    ├── audio.mp3
    └── cover.jpg
```

## 2. Upload the Files

Upload the entire folder to a compatible static hosting provider.

Examples:

- GitHub Pages
- Netlify
- Cloudflare Pages
- Vercel
- Other static hosting services

## 3. Open the Generated Page

Visit the URL provided by your hosting provider.

The generated player will load the local audio and artwork from:

```text
source/
```

No server-side application is required.

---

# 📁 Recommended Project Structure

A single generated player can use:

```text
my-song/
│
├── index.html
│
└── source/
    ├── audio.mp3
    └── cover.jpg
```

For multiple songs:

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

This structure works well for static websites and personal music collections.

---

# 🌐 Live Demo

Try MyLyricSong online:

**https://jproject-1.github.io/mylyricsong/**

No installation is required.

---

# 💻 Browser Compatibility

MyLyricSong uses modern browser features including:

- HTML5 Audio
- FileReader API
- Blob API
- `URL.createObjectURL()`
- `iframe srcdoc`
- Web Share API
- Clipboard API

Recommended browsers:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

Some features, especially native sharing, may behave differently depending on browser, operating system, and device.

---

# ⚠️ Known Considerations

## Audio Compatibility

The browser must be able to decode the selected audio format.

If a browser does not support a particular format, playback may fail.

---

## LRC Accuracy

Lyric synchronization depends on the timestamps contained in your LRC data.

For accurate synchronization, make sure the timestamps match the audio.

---

## Large Audio Files

MyLyricSong processes files inside the browser.

Very large files can require significant memory and may cause slower processing or browser limitations.

For best results, use reasonably sized audio files.

---

## Generated File Size

When exporting a ZIP package, the original audio and cover files are included.

Therefore:

```text
Larger audio
      ↓
Larger ZIP
```

---

## Browser Storage

MyLyricSong does not function as a cloud music-storage service.

Uploaded files are processed for the current generation/export workflow.

If you need permanent storage, store the exported project using your own storage or hosting solution.

---

# 🔐 Security Considerations

MyLyricSong is primarily a client-side application.

Because generated pages can contain user-provided information, you should only use content that you trust and are authorized to distribute.

When publishing generated pages:

- Review generated metadata.
- Review uploaded artwork.
- Review lyrics.
- Review credits.
- Review the selected license.
- Ensure that no private information is unintentionally included.
- Use a trusted hosting provider.

---

# 🤝 Contributing

Contributions are welcome.

You can contribute by:

- 🐛 Reporting bugs
- 💡 Suggesting features
- 🎨 Improving UI/UX
- 📝 Improving documentation
- 🎵 Improving lyric synchronization
- 🌐 Improving browser compatibility
- ♿ Improving accessibility
- ⚡ Improving performance
- 🔧 Submitting code improvements

For major changes, opening an issue first is recommended so the proposed change can be discussed before implementation.

---

# 📥 Distribution

MyLyricSong can be distributed through GitHub Releases.

The project is intentionally designed so users can obtain a ready-to-use release without cloning the Git repository.

Recommended distribution flow:

```text
Source Code
     │
     ▼
GitHub Repository
     │
     ▼
GitHub Release
     │
     ├── MyLyricSong.zip
     └── Other release assets
             │
             ▼
       User downloads
             │
             ▼
       Extracts & uses
```

This makes MyLyricSong suitable for users who simply want to download and use the template without learning Git.

---

# 📄 License

MyLyricSong source code is released under the **MIT License**.

```text
MIT License

Copyright (c) 2026 JASONPW

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

The **MIT License applies to the MyLyricSong source code/software**.

It does **not automatically apply** to:

- Music
- Lyrics
- Audio recordings
- Album artwork
- Artist names
- Trademarks
- Logos
- Third-party libraries
- Third-party assets
- User-created content

These materials may have separate copyrights, licenses, trademarks, or terms of use.

You are responsible for complying with all applicable licenses and rights for content used with MyLyricSong.

---

# 📚 Third-Party Libraries & Services

MyLyricSong uses or references several third-party technologies.

Examples include:

- Tailwind CSS
- Font Awesome
- JSZip
- Google Fonts
- Web APIs provided by modern browsers

Third-party libraries and services remain subject to their respective licenses and terms.

The MIT License for MyLyricSong does not override or replace third-party licenses.

---

# 🙏 Credits

## MyLyricSong

Created by:

**JASONPW & YCYLSTUDIO**

MyLyricSong was created as an independent browser-based music and lyric creation tool.

Special thanks to:

- The open-source community
- Web platform developers
- Browser developers
- Library maintainers
- Everyone who contributes feedback and improvements

---

# 📌 Disclaimer

MyLyricSong is an independent open-source project.

It is **not affiliated with, endorsed by, sponsored by, or officially connected to Spotify**.

Spotify and related trademarks are property of their respective owners.

MyLyricSong is provided as a tool for creating standalone music and lyric pages.

Users are solely responsible for the legality of the content they upload, generate, publish, and distribute.

The developers of MyLyricSong are not responsible for unauthorized use, copyright infringement, licensing violations, or illegal distribution of content created using the software.

---

# ⭐ Support the Project

If you find MyLyricSong useful, consider:

- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting features
- 🔧 Contributing improvements
- 📝 Improving documentation
- 📢 Sharing the project with other developers

Every contribution helps improve the project.

---

# 🎵 MyLyricSong

**Create. Sync. Play. Share.**

A lightweight, browser-based music and lyric page generator.

**Free to use. Open source. MIT licensed.**
