# Echo Mods

A mod manager for Echo VR: profiles, plugin and lobby mods, settings, and sharing by zip or profile code.

**[Download the latest EchoMods.zip](https://github.com/bollko/EchoModManager/releases/latest/download/EchoMods.zip)**: unzip it anywhere you can write to, then run `EchoMods.exe`. Nothing else to install.

Guide, mods and the Lobby Mod Kit: https://echo-mods.echoreels.workers.dev

Windows may warn that the app is from an unknown publisher: choose **More info**, then **Run anyway**.

This repository holds the releases. Echo Mods is not made by or affiliated with Ready At Dawn or Meta.

## What's new

**v1.1.2**
- Add Content works on PCs where it said it could not reach the website: when Python's own HTTPS check fails (Windows had not fetched the site's root certificate yet), Echo Mods asks again through Windows' own curl. If it still cannot connect, the message says why, and `%APPDATA%\EchoMods\app.log` has the details.

**v1.1.1**
- Brings its own plugin loader (dinput8.dll) and adds it when you install a plugin mod and nothing in the game loads plugins yet. Another dinput8.dll mod you already have (ReShade, ...) keeps working: it is loaded through the new one.

**v1.1.0**
- Mod dependencies: a mod can list the mods it needs (`"requires"` in mod.json). Installing it also installs the missing ones from the Echo Mods website and switches them on together; the mod list says when one is missing.
- Warns when a plugin mod is installed on a game without the plugin loader.
- Lobby mods: doorways cut through lobby walls (`CUT_` boxes), live screens (`LIVE_` materials) and moving parts (`ANIM_` objects) for mods with a plugin; Blender models stay visible deep inside a lobby mod's own rooms.
