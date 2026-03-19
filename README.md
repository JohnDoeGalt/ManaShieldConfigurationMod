# Mana Shield Mod v1.2.0
### for Tainted Grail: The Fall of Avalon

## Description

This mod reverts the Mana Shield regeneration changes introduced in patch 1.20.

The 1.20 update added two penalties to Mana Shield:
1. A delay before mana regenerates after taking a hit
2. Reduced mana regeneration (1:1 with Mana Shield value) while in combat

This mod lets you configure or disable both penalties via an in-game settings menu.

## Features

- Configurable combat mana regen penalty (0% to 100%)
- Toggle for post-hit regen delay (on/off)
- Settings accessible in: **Game Options > Gameplay > Mana Shield Mod Settings**
- Works in multiplayer (settings sync between players)

## Requirements

- Tainted Grail: The Fall of Avalon (Steam version)
- [BepInEx 5.x (Mono build)](https://github.com/BepInEx/BepInEx/releases) - Use the "BepInEx_win_x64" Mono version, NOT IL2CPP

## Installation (Manual)

1. **Install BepInEx 5.x Mono** if not already installed:
   - Download BepInEx_win_x64 from the releases page
   - Extract to your game folder (where "Fall of Avalon.exe" is located)
   - Run the game once
   - Close the game

2. **Copy the mod:**
   - Download the latest release
   - Copy the `BepInEx` folder to your game directory
   - The DLL should end up at: `<GameFolder>/BepInEx/plugins/ManaShieldRevert.dll`

## Installation (Vortex/Nexus Mod Manager)

1. Make sure BepInEx 5.x Mono is installed (see above)
2. Use "Mod Manager Download" or drag the ZIP into Vortex
3. Enable the mod

## Uninstallation

Simply delete: `<GameFolder>/BepInEx/plugins/ManaShieldRevert.dll`

Or disable/remove via your mod manager.

## Configuration

All settings are available in-game:
**Main Menu > Options > Gameplay > Mana Shield Mod Settings**

| Setting | Description |
|---------|-------------|
| Enable Mana Shield Mod | Master toggle for the mod |
| Combat Regen Penalty | 0% (no penalty) to 100% (vanilla 1.20 behavior) |
| Post-Hit Regen Delay | OFF (no delay) or ON (vanilla 1.20 behavior) |

Default settings restore pre-1.20 behavior (no penalties).

## Compatibility

- Works with game version 1.20+
- Should work with other BepInEx mods
- Multiplayer compatible (settings sync)

## Troubleshooting

**Q: Mod doesn't load**
A: Make sure you're using BepInEx Mono (not IL2CPP). Check `BepInEx/LogOutput.log` for errors. The log should show "Mana Shield Revert" loading.

**Q: Settings don't appear in menu**
A: Make sure you're looking in Gameplay settings in the Main Menu, not after loading your game. Try restarting the game. Check the log for "settings injected" message.

**Q: Game crashes on startup**
A: Verify BepInEx is installed correctly. Try deleting `BepInEx/cache` folder.

## Credits

- **Mod Author:** [JohnDoeGalt117](https://www.nexusmods.com/users/JohnDoeGalt117) (Nexus Mods)
- Built with BepInEx and HarmonyLib

## Changelog

### v1.2.0
- Fixed mana bar visual indicator showing incorrect regen prediction
- Visual now correctly reflects mod settings (no more false "drain" effect)

### v1.1.0
- Added in-game settings menu
- Configurable combat regen penalty (slider)
- Configurable post-hit delay (toggle)

### v1.0.0
- Initial release
- Removes post-hit mana regen delay
- Removes combat mana regen penalty

## License

This mod is provided as-is for personal use. Feel free to modify for your own use. Please credit if redistributing.
