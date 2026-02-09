# GiveWeapon Plugin for Counter-Strike 2

CS2 plugin that allows admins to give weapons to players via console command.

## Requirements

- CounterStrikeSharp installed on your CS2 server

## Installation

1. Copy `GiveWeapon/GiveWeapon.dll` to your CS2 server:
   ```
   csgo/addons/counterstrikesharp/plugins/
   ```

## Usage

In server console, use the command:

```
gg_give_weapon <player_name|steam_id> <weapon_name>
```

You can identify players by:
- **Player name** - exact or partial match (case insensitive)
- **SteamID64** - the 17-digit Steam ID

### Examples

```
# By player name
gg_give_weapon Player123 weapon_famas
gg_give_weapon Player123 weapon_ak47
gg_give_weapon Player123 famas          # "weapon_" prefix is optional

# By SteamID64
gg_give_weapon 76561198012345678 weapon_awp
gg_give_weapon 76561198012345678 deagle
```

## Console Output

The plugin provides detailed console output for all operations:

### Success example:
```
[GiveWeapon] Command received: gg_give_weapon
[GiveWeapon] Target: 'Player123', Weapon: 'weapon_famas'
[GiveWeapon] Searching by name: 'Player123'
[GiveWeapon] Found exact name match: Player123
[GiveWeapon] Found player: Player123 (SteamID: 76561198012345678)
[GiveWeapon] SUCCESS: Gave 'weapon_famas' to 'Player123' (SteamID: 76561198012345678)
```

### Error examples:
```
[GiveWeapon] ERROR: Player 'UnknownPlayer' not found!
[GiveWeapon] ERROR: Player 'Player123' is not alive!
[GiveWeapon] ERROR: Invalid weapon name 'weapon_invalid'!
```

## Available Weapons

### Rifles
- `weapon_ak47` - AK-47
- `weapon_m4a1` - M4A1
- `weapon_m4a1_silencer` - M4A1-S
- `weapon_famas` - FAMAS
- `weapon_galilar` - Galil AR
- `weapon_aug` - AUG
- `weapon_sg556` - SG 553

### SMGs
- `weapon_mp9` - MP9
- `weapon_mac10` - MAC-10
- `weapon_mp7` - MP7
- `weapon_mp5sd` - MP5-SD
- `weapon_ump45` - UMP-45
- `weapon_p90` - P90
- `weapon_bizon` - PP-Bizon

### Shotguns
- `weapon_nova` - Nova
- `weapon_xm1014` - XM1014
- `weapon_sawedoff` - Sawed-Off
- `weapon_mag7` - MAG-7

### Machine Guns
- `weapon_m249` - M249
- `weapon_negev` - Negev

### Pistols
- `weapon_glock` - Glock-18
- `weapon_usp_silencer` - USP-S
- `weapon_hkp2000` - P2000
- `weapon_p250` - P250
- `weapon_fiveseven` - Five-SeveN
- `weapon_tec9` - Tec-9
- `weapon_cz75a` - CZ75-Auto
- `weapon_deagle` - Desert Eagle
- `weapon_revolver` - R8 Revolver
- `weapon_elite` - Dual Berettas

### Sniper Rifles
- `weapon_awp` - AWP
- `weapon_ssg08` - SSG 08
- `weapon_scar20` - SCAR-20
- `weapon_g3sg1` - G3SG1

### Equipment
- `weapon_hegrenade` - HE Grenade
- `weapon_flashbang` - Flashbang
- `weapon_smokegrenade` - Smoke Grenade
- `weapon_molotov` - Molotov
- `weapon_incgrenade` - Incendiary Grenade
- `weapon_decoy` - Decoy Grenade
- `weapon_knife` - Knife
- `weapon_taser` - Zeus x27

## Permissions

This command requires `@css/cheats` permission. Make sure the admin executing the command has this permission in the CounterStrikeSharp admin config.

## License

MIT License
