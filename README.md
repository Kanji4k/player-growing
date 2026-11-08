# Player Spotter (Fabric, Minecraft 1.21.11)

Client-side mod. It makes other players glow, shows their name, and shows a distance
meter with an arrow pointing down at their head. Nothing is sent to the server, so it
needs no server install and works on any multiplayer server.

## Features
- Glow on other players, with your own color (presets or RGB sliders)
- Name above the head (server/tab/team name, or plain account name)
- Distance meter `[|||||     ]` with meters text, **on/off**
- Auto fill: the bar fills as the player gets closer (off = always full)
- Arrow pointing down to the head, **on/off**
- Range slider **1 to 16 chunks** (glow, names, meter and arrow all follow it)
- Master on/off, everything saved in `config/playerspotter.json`
- Settings screen from **Mod Menu** (Configure button) or the **K** key
- **V** key turns the whole mod on/off

## Build
You need Java 21.

```
gradle wrapper --gradle-version 9.2.1     # only once, if there is no gradlew yet
./gradlew build                           # Windows: gradlew.bat build
```

The mod jar is `build/libs/player-spotter-1.0.0.jar`. Put it in `.minecraft/mods`
with Fabric Loader 0.17.3+ and Fabric API for 1.21.11. Mod Menu is optional
(but needed for the Configure button).

## Notes
- You can only see players the server has loaded for you, so the real maximum is the
  server's view distance even if the slider says 16.
- The arrow position is exact in first person. In third person it follows your head,
  not the camera.
- Many servers (Hypixel, competitive/PvP servers) ban glow/ESP style mods. Use it where it is allowed.
