# NAS TV

An Android TV app for browsing and playing the photos, videos and music stored on a NAS. It reads
the shared folders directly over SMB 3, so no media server has to run on the NAS.

Developed and tested with a Synology NAS and a Xiaomi Mi TV Stick 4K.

## Features

- **Browsing**: the NAS's shared folders with thumbnails (Synology's own thumbnails are used when
  the folder has them); large, compact or details view; sorting by name or by capture date; a
  start folder of your choice.
- **Photos**: full-screen viewer with zoom, pan and photo details (date, camera, resolution);
  photos that show sideways can be rotated, and stay rotated on this TV.
  JPEG, PNG, WebP, HEIF, GIF and BMP.
- **Videos**: playback with resume, subtitles from `.srt`, `.ass` and `.vtt` files next to the
  video, choice of audio and subtitle tracks, and correct audio timing for AVI (DivX/Xvid) files.
- **Music**: playback continues while you browse; a whole folder (sub-folders included) can be played
  at once; songs and folders from anywhere can be played next or added to the queue, and removed
  from it; shuffle, repeat, equalizer (where the TV supports it), sleep timer, album art and a
  visualiser that follows the music. Long tracks such as audiobooks resume where they were left.
- **Hiding**: files and folders can be hidden from the browser on this TV. The NAS is not changed.
- **Burn-in care for OLED TVs**: still screens move by a few pixels and dim after a while without
  input.
- **Options**: hold OK (or press Menu) on any screen for the actions available there: queueing,
  hiding, view and sort settings, and the music controls, without leaving what you are doing.
- **Remote**: everything works with the D-pad; Back first returns to the top of a long folder; media
  keys control the music from any screen.

## Requirements

- An Android TV or Google TV device running Android 11 or later.
- A NAS or computer sharing folders over SMB 3 with encryption enabled, and a user account
  (guest access is not used).

## Installation

1. Download `NasTV-<version>.apk` from the [Releases](../../releases) page.
2. Install it on the TV, for example with a file-sending app or a downloader app. Android asks you to
   allow installing apps from that source.
3. Open NAS TV and enter the NAS address, the shared folders, your user name and your password.

To check that a download is the original file, compare its SHA-256 checksum with the one in the
release notes. Every release is signed with the same certificate:

```
SHA-256: C1:C6:3E:B6:B4:57:04:6B:F8:40:7F:83:2D:63:9D:CC:97:E4:AD:2F:01:1F:A6:C3:A3:3B:D8:19:09:78:48:92
```

## Privacy and security

NAS TV talks only to the NAS you configure. It has no accounts, no analytics, no advertising and no
servers of its own: nothing about you or your files is sent anywhere else.

- Connections use SMB 3 with signing and encryption required; the app refuses unencrypted and guest
  connections.
- The NAS is identified when you first connect. If a different server answers later, the app stops
  before sending the password and tells you.
- The password and the thumbnail cache are encrypted on the TV and excluded from backups.

## Licence

Copyright © 2026 Damiano Chiappa. All rights reserved.

NAS TV is proprietary software, free to use for personal purposes; see [LICENSE.md](LICENSE.md). The source code is not
published. The open-source components it includes are listed, with their licences, in
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

NAS TV is an independent project, not affiliated with Google, Synology or Xiaomi.
