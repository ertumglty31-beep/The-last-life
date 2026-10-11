# The Last Life — Forge 1.20.1 prototype

This is the first source-code prototype for The Last Life.

## Included
- Registers a wearable `Gaz Maskesi` item (`thelastlife:gas_mask`).
- Gives each player a gas mask the first time they join a world (main hand if empty, otherwise inventory).
- If the mask is equipped in the helmet slot, the gas countdown resets to zero.
- If the mask is not equipped, a 10-second (200 game tick) countdown starts.
- The player receives a warning every second and dies when the countdown reaches zero.
- Creative and spectator players are exempt.

## Target
- Minecraft Java Edition 1.20.1
- Minecraft Forge 47.x
- Java 17 for building

## Build
This folder is a Gradle Forge project, not a ready-to-install `.jar` yet. With Gradle installed and internet access to download Forge Gradle dependencies, run:

```sh
gradle build
```

The built mod jar will be in `build/libs/`.

## Important prototype notes
- The item currently uses Minecraft's leather-helmet armor model. A custom 3D gas-mask model/armor texture is not included yet.
- This project has not been compiled or tested in Minecraft in this environment. Build and in-game testing are required before treating it as a working release.
- The first-join mask is granted once per player save. If the player loses it, it is not automatically replaced.
