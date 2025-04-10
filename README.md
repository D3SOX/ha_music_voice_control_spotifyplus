# 🎧 Home Assistant Spotify Voice Control Automations

This repository contains a collection of **Home Assistant automations** that enable **voice-controlled Spotify playback** via custom conversation triggers.  
With these automations, you can **play music**, **adjust volume**, and **control playback effortlessly**.

> ⚠️ **Note:** Currently, this automation is available **only in English and German**.  
> I'd be happy if someone contributes a yaml with the **other translation** of the voice commands. 😊

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
  - *German:* `"Pause Spotify"`, `"Nächstes Lied"`, `"Vorheriges Lied"`, `"Shuffle an"`, `"Wiederholung an"`, `"Lautstärke auf 50%"`  
  - *English:* `"Pause Spotify"`, `"Next song"`, `"Previous song"`, `"Shuffle on"`, `"Repeat on"`, `"Volume to 50%"`

- **Like/Dislike Songs**  
  *Example (DE):* `"Ich mag dieses Lied"` or `"Ich mag dieses Lied nicht"`  
  *Example (EN):* `"I like this song"` or `"I don't like this song"`

- **Change Playlists**  
  *Example (DE):* `"Spiele etwas anderes"`  
  *Example (EN):* `"Play something else"`

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

6. **Voice: Play Weekly Spotify Playlist**  
   🔄 *Plays your weekly Spotify playlist (Discover Weekly).*

7. **Voice: Lautstärke ändern**  
   🔊 *Adjusts the volume (up, down, or to a specific percentage).*

8. **Voice: Nächstes Lied**  
   ⏭️ *Skips to the next song.*

9. **Voice: Vorheriges Lied**  
   ⏮️ *Goes back to the previous song.*

10. **Voice: Zufällige Wiedergabe**  
    🔀 *Toggles shuffle on or off.*

11. **Voice: Toggle Repeat Mode**  
    🔁 *Toggles repeat mode on or off.*

12. **Voice: Spotify abspielen / Play**  
    ▶️ *Starts Spotify playback.*

13. **Voice: Spiele Playlist - v2**  
    📂 *Plays a specific playlist, optionally in shuffle mode.*

14. **Voice: Like Current Song**  
    ⭐ *Marks the currently playing song as a favorite.*

15. **Voice: Dislike Current Song**  
    👎 *Removes the currently playing song from favorites.*

16. **Voice: Pause Spotify**  
    ⏸️ *Pauses or stops Spotify playback.*

17. **Voice: Play Something Else**  
    🔄 *Changes to a different playlist in the same genre/category.*

---

## 🚀 Getting Started

### ✅ Prerequisites

> [!IMPORTANT]  
> There are multiple integrations called Spotify Plus. Make sure to use the one linked here

- **Home Assistant** with **[SpotifyPlus](https://community.home-assistant.io/t/spotifyplus-integration/698651)** ( Big thanks to @thlucas )
- **Recommended hardware: [Home Assistant Voice Preview Edition (VPE)](https://www.home-assistant.io/voice-pe/)**
- Adjust entity IDs (e.g. `media_player.spotifyplus_nico`, `media_player.home_assistant_voice_099b20_media_player`, `script.play_spotify_on_nico_source`) as needed.

### 🔧 Configuration

Add the following in your

- `configuration.yaml`: [voice_spotifyplus_configuration.yaml](voice_spotifyplus_configuration.yaml)
- `automations.yaml`: [voice_spotifyplus_automations.yaml](voice_spotifyplus_automations.yaml)
- `scripts.yaml`: [voice_spotifyplus_scripts.yaml](voice_spotifyplus_scripts.yaml)


## 📢 Contributing
Feel free to fork, translate, suggest improvements, or add new automations!
Contributions are always welcome. 😊

For more details, check out the discussion here:
👉 [Home Assistant Community Forum](https://community.home-assistant.io/t/voice-music-control-with-spotifyplus-and-ha-voice-pe/837357)
