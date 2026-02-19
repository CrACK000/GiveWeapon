# GiveWeapon

Counter-Strike 2 plugin for [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp) that gives weapons to players at round start.

## Features

- **Round Start Weapons** - Automatically give configured weapons to all players
- **Knife Only Mode** - Strip all weapons and give only knife
- **Team Filters** - Enable/disable for Terrorists and Counter-Terrorists separately
- **Armor Support** - Give kevlar and helmet
- **Custom Weapons** - Optionally allow players to keep purchased weapons
- **Bomb Preservation** - Terrorists always keep their bomb on bomb defusal maps
- **Disabled by Default** - Plugin is disabled until explicitly enabled

## Installation

1. Install [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp)
2. Download `GiveWeapon.dll`
3. Copy to your server:
   ```
   csgo/addons/counterstrikesharp/plugins/GiveWeapon/GiveWeapon.dll
   ```
4. Restart the server

## Configuration

Config file location:

```
csgo/addons/counterstrikesharp/configs/plugins/GiveWeapon/GiveWeapon.json
```

```json
{
  "enabled": false,
  "round_start_weapons": ["weapon_ak47", "weapon_deagle"],
  "allow_custom_weapons": false,
  "knife_only_mode": false,
  "give_to_terrorists": true,
  "give_to_counter_terrorists": true
}
```

| Option                       | Default                            | Description                             |
| ---------------------------- | ---------------------------------- | --------------------------------------- |
| `enabled`                    | `false`                            | Enable/disable the plugin               |
| `round_start_weapons`        | `["weapon_ak47", "weapon_deagle"]` | Weapons to give at round start          |
| `allow_custom_weapons`       | `false`                            | Allow players to keep purchased weapons |
| `knife_only_mode`            | `false`                            | Give only knife                         |
| `give_to_terrorists`         | `true`                             | Give weapons to Terrorists              |
| `give_to_counter_terrorists` | `true`                             | Give weapons to Counter-Terrorists      |

## Commands

| Command                   | Usage                               | Description                    |
| ------------------------- | ----------------------------------- | ------------------------------ |
| `gg_plugin`               | `gg_plugin <1/0>`                   | Enable/disable the plugin      |
| `gg_set_round_weapons`    | `gg_set_round_weapons <weapons>`    | Set round start weapons        |
| `gg_give_weapon`          | `gg_give_weapon <target> <weapons>` | Give weapon(s) to player(s)    |
| `gg_knife_only`           | `gg_knife_only <1/0>`               | Enable/disable knife only mode |
| `gg_allow_custom_weapons` | `gg_allow_custom_weapons <1/0>`     | Allow purchased weapons        |
| `gg_status`               | `gg_status`                         | Show current settings          |

### Target Selectors

`@all`, `@t`, `@ct`, `@alive`, `@dead`, `<name>`, `<steamid>`

### Examples

```
gg_plugin 1
gg_set_round_weapons ak47,deagle,assaultsuit
gg_give_weapon @all awp
gg_knife_only 1
```

## Supported Weapons

**Primary:** `ak47`, `m4a1`, `m4a1_silencer`, `famas`, `galilar`, `aug`, `sg556`, `mp9`, `mac10`, `mp7`, `mp5sd`, `ump45`, `p90`, `bizon`, `nova`, `xm1014`, `sawedoff`, `mag7`, `m249`, `negev`, `awp`, `ssg08`, `scar20`, `g3sg1`

**Secondary:** `glock`, `usp_silencer`, `hkp2000`, `p250`, `fiveseven`, `tec9`, `cz75a`, `deagle`, `revolver`, `elite`

**Grenades:** `hegrenade`, `flashbang`, `smokegrenade`, `molotov`, `incgrenade`, `decoy`

**Armor:** `kevlar`, `assaultsuit`

> Weapon names work with or without `weapon_` prefix

## Notes

- Plugin is **disabled by default**
- **Bomb is always preserved** - T players keep their bomb
- Late spawning players also receive the loadout

## Requirements

- Counter-Strike 2 Dedicated Server
- [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp)

## License

MIT License
