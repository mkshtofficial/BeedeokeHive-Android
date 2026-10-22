<div align="center">

<img src="https://github.com/mkshtofficial/BeedeokeHive/blob/main/beedeokehive.png" alt="Beedeoke Hive" width="112" />

# Beedeoke Hive for Android

**Make Karaoke Singers Hit Tunes**

Your karaoke library, live microphone, music, videos, and recordings in one place.

**Android 10+ · Phones & tablets · Android/Smart TV remote navigation**

</div>

---

Beedeoke Hive brings karaoke playback, song search, reservations, and personal media playback to Android. Use your own content, organize your favorites, and control playback with touch or a compatible TV remote.

## Features

### Karaoke

- Find songs by code, title, or singer.
- Browse artists, Favorite Songs, and New Songs from the main menu.
- Reserve songs, play a reservation immediately, or remove it from the queue.
- Play supported MIDI/KAR, MP3+MIDI, MP3+CDG, and MP4 content.
- Choose a SoundFont for MIDI playback and adjust key, tempo, and melody level.
- Customize lyrics, background videos/photos, and bottom text.
- Place the landscape search panel on the left, center, or right.

### Media Player

- **Videos:** browse MTV files from your video directory.
- **MP3:** browse audio files and watch an audio-reactive spectrum display.
- **Recordings:** play videos saved by the app.
- View filenames and durations, seek, use previous/next, and switch between Fit and Zoom.
- Automatically continue to the next file and stop at the end of the playlist.
- Keep Media Player audio playing after pressing Home, with notification playback controls.

### Live microphone (Wired Earphones/Mic)

Sing along in KTV using the device microphone or a compatible Beedeoke SmartLink microphone on the same local network.

Open **Settings → Audio → MICROPHONE**:

- **Microphone Source:** choose **Smart Link Mic Only**, **Device Mic Only**, or **Use Both**. The default source is Smart Link.
- **Microphone Stream:** choose **Disabled**, **Enabled with Standby** (active while a song is playing), or **Enable (Always On)** (also active while KTV is idle). Streaming is disabled by default.
- Adjust **Mic Volume**, **Echo**, **Reverb**, **Delay**, **Clarity**, and **Sensitivity (threshold)**.

For the device microphone, select **Device Mic Only** or **Use Both**, enable streaming, and allow microphone access when prompted. For SmartLink, connect the compatible controller and use its microphone feature.

### Picture-in-Picture

Enable **Settings → MP3 | MTV Settings → Enable Picture-in-Picture**. During active Media Player video or KTV playback, press **Home** to open the floating player on supported devices.

KTV's PiP window shows the playback scene and lyrics without its keypad or search panels. MP3 playback continues through the background Media Player service.

### Recording and remote control

- Record karaoke sessions and choose the recording directory and quality.
- Browse completed recordings in the Media Player.
- Use compatible Beedeoke SmartLink controls on the same local network.
- Choose an optional remote password; an empty password allows connections without a password.

## Getting started

1. Install the Android APK provided with the release.
2. Open Beedeoke Hive and select the resources location, or download resources when prompted.
3. Grant access to your selected folder if Android requests it.
4. Complete app activation when required. Protected song libraries can require separate library activation.
5. Open **Enter KTV**, **Song Search**, or **Media Player** from the main menu.

An activated app does not automatically activate every protected library. If **Library Activation Required** appears, activate that library or choose **Don't Use the Library** to continue with available user content.

## Resources folders

The usual resources layout is:

```text
BeedeokeHive/
├── idx/                 # Protected catalog files and optional newsongs.lst
├── songs/               # Your song files, subfolders, and supported ZIP archives
├── soundfont/           # SF2 SoundFonts for MIDI playback
├── bgv/                 # Karaoke background videos
├── bgphoto/             # Karaoke background images
├── mp3/                 # Standalone MP3 files
├── videos/              # MTV / MP4 videos
└── recordings/          # Default recording destination
```

You can choose different MP3 and MTV directories under **MP3 | MTV Settings**. Recording and background-video directories also have their own settings. Existing files stay in their selected locations.

Use **Refresh User Content** after adding or changing songs. Catalog caching helps avoid repeatedly reading unchanged ZIP contents; ZIP size and last-modified time are checked for changes.

### Song files and ZIP archives

Supported song combinations include `.mid`, `.midi`, `.kar`, `.mp4`, `.mp3`, matching `.mp3` + `.cdg`, and matching `.mp3` + MIDI/KAR files. Files inside subfolders and supported ZIP archives can also be indexed.

For example:

```text
songs/
├── My Song - Artist.mid
├── Karaoke Track.mp3
├── Karaoke Track.cdg
└── Collection.zip
    └── songs/Another Song - Artist.mid
```

Matching audio, graphics, and lyric files should use the same filename stem. Playback depends on the file being valid and on device codec support.

### New Songs

Create **`idx/newsongs.lst`** using this format:

```text
N="41587",T="California Rain",S="None"
N="41588",T="Permanent Scars",S="None"
N="41589",T="Breathe In, Breathe Out",S="None"
```

| Field | Meaning |
| --- | --- |
| `N` | Song code in the loaded catalog |
| `T` | Display title |
| `S` | Display singer |

The **New Songs** menu displays matching catalog entries in file order. The idle showcase uses this list when it contains available songs; otherwise, it keeps the default showcase. Duplicate, malformed, and unavailable codes are skipped.

Restart the app or use **Refresh User Content** after editing the file. Save it as UTF-8.

## Touch and TV controls

| Action | Control |
| --- | --- |
| Select a song or button | Tap, or press OK |
| Move between controls and results | D-pad arrows |
| Favorite or unfavorite a song | Tap its heart, or hold OK on a song result |
| Return or close a panel | Back |
| Show fullscreen Media Player controls | Tap the video, or press a remote button |
| Open PiP when enabled | Press Home during supported playback |

TV storage access, folder pickers, and PiP availability vary by Android version and device firmware. App storage is an alternative when a device cannot grant access to a shared folder. Files stored in app storage are removed when the app is uninstalled.

## Troubleshooting

**Resources not found:** select an accessible resources folder or use the resource download option. Confirm that the selected folder still exists and that its access permission is valid.

**No songs after adding files:** check the folder, refresh user content, and confirm that the files use a supported format. New Songs codes must already exist in the loaded catalog.

**Cannot select the internal-storage root:** choose or create a subfolder such as `BeedeokeHive` instead.

**No MIDI instruments:** select a valid `.sf2` SoundFont and check playback volume.

**No microphone audio:** check the selected microphone source, enable Microphone Stream, and check Mic Volume. Allow microphone access for the device mic, or check the SmartLink connection for a remote mic. In standby mode, start a song first. Lower the sensitivity threshold if quiet singing is being cut off.

**PiP does not open:** enable the setting, start playback, and check whether the device supports and allows Picture-in-Picture for Beedeoke Hive.

## Feedback

When reporting an issue, include the app version, device model, Android version, steps to reproduce, and the affected file format. Screenshots or short recordings are helpful. Do not include private song files in public reports.

Use music and other content that you own or have permission to use.
