# RemoveAmbientSound — FiveM Script

![Version](https://img.shields.io/badge/version-1.0.0-blue)
[![Download](https://img.shields.io/github/v/release/Carontedev/RemoveAmbientSound-FiveM?label=download)](https://github.com/Carontedev/RemoveAmbientSound-FiveM/releases/latest)

**Remove all ambient sounds from GTA V in FiveM.**  
Made by **CaroStudio** — apocalyptic, zombie or silent roleplay servers.

Silences city, traffic, sirens, horns, peds, music, ocean, random events and dispatch services. No config, plug & play.

## Installation

1. Download the [latest release](https://github.com/Carontedev/RemoveAmbientSound-FiveM/releases/latest)
2. Extract `RemoveAmbientSound` into your server's `resources/` folder
3. Add to `server.cfg`:

```
ensure RemoveAmbientSound
```

4. Full server restart (do not use `restart`, requires full restart for audio banks)

## What it disables

| Category | Method |
|---|---|
| City ambience | Audio scenes (CHARACTER_CHANGE_IN_SKY_SCENE, FBI_HEIST_H5_MUTE_AMBIENCE_SCENE, DLC_MPHEIST_TRANSITION_TO_APT_FADE_IN_RADIO_SCENE) |
| Traffic & peds | Density multipliers set to 0 every frame |
| Vehicle horns | OverrideVehHorn on all NPC vehicles every 1s |
| Distant sirens | DistantCopCarSirens(false) every frame |
| Police scanner | SetAudioFlag |
| Flight music | SetAudioFlag |
| Ocean sounds | SetDeepOceanScaler(0.0) |
| Ambient speech | SetAudioFlag("DisableBarks") |
| Static emitters | Strip club and other location-based emitters |
| Scenario vehicles | Race, police, military, mechanic scenarios disabled |
| Ambient zones | Island disabled zones |
| Police dispatch | All 15 dispatch services disabled |
| Random events | Disabled |
| Garbage trucks & cops | Spawning disabled |

## Compatibility

- Any framework (ESX, QBCore, standalone)
- Client-side only — zero performance impact

## Credits

Base by [DikaN1337/fivem-disableambientsounds](https://github.com/DikaN1337/fivem-disableambientsounds) — improvements and maintenance by **CaroStudio**.
