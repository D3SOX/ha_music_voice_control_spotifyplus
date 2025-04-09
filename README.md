# 🎧 Home Assistant Spotify Voice Control Automations

This repository contains a collection of **Home Assistant automations** that enable **voice-controlled Spotify playback** via custom conversation triggers.  
With these automations, you can **play music**, **adjust volume**, and **control playback effortlessly**.

> ⚠️ **Note:** Currently, this automation is available **only in English and German**.  
> I’d be happy if someone contributes a yaml with the **other translation** of the voice commands. 😊

---

## 🎵 Features

- **Play Music by Artist**  
  *Example (DE):* `"Spiele Musik von Queen"`  
  *Example (EN):* `"Play music by Queen"`

- **Play Specific Songs**  
  *Example (DE):* `"Spiele den Song Bohemian Rhapsody"`  
  *Example (EN):* `"Play the song Bohemian Rhapsody"`

- **Play Podcasts**  
  *Example (DE):* `"Starte den Podcast Fest & Flauschig"`  
  *Example (EN):* `"Start the podcast Fest & Flauschig"`

- **Artist Radio & Playlists**  
  *Example (DE):* `"Spiele das Radio von Coldplay"` or `"Spiele die Playlist Party Hits"`  
  *Example (EN):* `"Play the radio of Coldplay"` or `"Play the playlist Party Hits"`

- **Control Playback**  
  Commands:  
  - *German:* `"Pause Spotify"`, `"Nächstes Lied"`, `"Shuffle an"`, `"Lautstärke auf 50%"`  
  - *English:* `"Pause Spotify"`, `"Next song"`, `"Shuffle on"`, `"Volume to 50%"`

- **Like Songs**  
  *Example (DE):* `"Ich mag dieses Lied"`  
  *Example (EN):* `"I like this song"`

---

## 📋 Automations Overview

1. **Voice: Spiele Musik von <Artist>**  
   🎤 *Plays music from a specific artist.*

2. **Voice: Spiele Song <Song>**  
   🎵 *Plays a specific song.*

3. **Voice: Spiele Podcast <Podcast>**  
   🎙️ *Plays a specific podcast.*

4. **Voice: Spiele Radio von <Artist>**  
   📻 *Plays the radio of a specific artist.*

5. **Voice: Spiele Spotify und Lieblingssongs**  
   ❤️ *Plays your favorite songs.*

6. **Voice: Spiele Spotify Weekly**  
   🔄 *Plays your weekly Spotify playlist (Spotify Weekly).*

7. **Voice: Lautstärke ändern**  
   🔊 *Adjusts the volume (up, down, or to a specific percentage).*

8. **Voice: Nächstes Lied**  
   ⏭️ *Skips to the next song.*

9. **Voice: Zufällige Wiedergabe**  
   🔀 *Toggles shuffle on or off.*

10. **Voice: Spotify abspielen / Play**  
    ▶️ *Starts Spotify playback.*

11. **Voice: Spiele Playlist - v2**  
    📂 *Plays a specific playlist, optionally in shuffle mode.*

12. **Voice: Like Current Song**  
    ⭐ *Marks the currently playing song as a favorite.*

13. **Voice: Pause Spotify**  
    ⏸️ *Pauses or stops Spotify playback.*

---

## 🚀 Getting Started

### ✅ Prerequisites

- **Home Assistant** with **[SpotifyPlus](https://community.home-assistant.io/t/spotifyplus-integration/698651)** ( Big thanks to @thlucas )
- **Recommended hardware: [Home Assistant Voice Preview Edition (VPE)](https://www.home-assistant.io/voice-pe/)**
- Adjust entity IDs (e.g., `media_player.spotify_nico`) and Spotify IDs/links as needed.
- Add the following helpers and scripts in your `configuration.yaml`:

### 🔧 Helpers Configuration

Copy from [voice_spotifyplus_configuration.yaml](voice_spotifyplus_configuration.yaml)

### 🔧 Scripts Configuration

- Script to select correct spotify source, if needed. (script.play_spotify_on_yourID_source)

```yaml
sequence:
  - alias: Update Source
    if:
      - condition: not
        conditions:
          - condition: state
            entity_id: media_player.spotifyplus_yourID
            attribute: source
            state: your-source (nico-pc for me)
    then:
      - data:
          source: your-source (nico-pc for me)
        target:
          entity_id: media_player.spotifyplus_yourID
        action: media_player.select_source
      - action: spotifyplus.player_set_shuffle_mode
        metadata: {}
        data:
          state: true
          entity_id: media_player.spotifyplus_yourID
    enabled: true
alias: Play Spotify on your Source
mode: single
icon: mdi:spotify
description: ""
```

### Import Blueprint

### **🔗 Direct Import via Home Assistant**
<a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FD3SOX%2Fha_music_voice_control_spotifyplus%2Fblob%2Fmain%2Fvoice_spotify_control.yaml" target="_blank" rel="noreferrer noopener"><img src="https://my.home-assistant.io/badges/blueprint_import.svg" alt="Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled." /></a>


📢 Contributing
Feel free to fork, translate, suggest improvements, or add new automations!
Contributions are always welcome. 😊

For more details, check out the discussion here:
👉 [Home Assistant Community Forum](https://community.home-assistant.io/t/voice-music-control-with-spotifyplus-and-ha-voice-pe/837357)
