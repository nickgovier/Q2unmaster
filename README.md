# Quake 2 Unmaster Mod

This mod gives you the ability to turn on/off some of the more significant gameplay tweaks of the Nightdive Studios remaster of Quake 2, to your taste.

It also allows you to choose a tweaked version of the berserker jump (by setting `un_berserker_jump` to 2), which adds a crouch/hunker down just before it jumps, and reduces the splash damage.

The mod is available to download at https://www.nexusmods.com/quake2/mods/15


## Source code

The source code for this mod is available at https://github.com/nickgovier/Q2unmaster

It is derived from the Nightdive game source release at: https://github.com/id-Software/quake2-rerelease-dll

Please see the Nightdive game source release `README.md` for compilation instructions and dependencies.

It is licensed under the GNU General Public License v2.0.  Please see `LICENSE.txt` for further info.


## Installation

Unzip the contents into `%USERPROFILE%\Saved Games\Nightdive Studios\Quake II\`
It should create an `unmaster` folder in there, alongside the existing `baseq2`

Launch the game with the command line parameter:

`+set game unmaster`

Or in Steam, click the Cog on the Quake 2 page, go to Properties, and enter:

`+set game unmaster`

in the Launch Options.


## Save games

It is recommended that you start a new game and create new saves for this mod.  However, some users have reported that they have been able to copy their saves from baseq2\save into the unmaster\save folder and continue their saved games using the mod.  However, given that the underlying code is changing, it is not guaranteed that this will work flawlessly.  As long as you retain a copy of your saves in baseq2\save, you can always continue those saved games without the mod.


## New cvars

Each change can be individually enabled or disabled with a console variable.  All of the Unmaster console variables are prefixed with `un_`. Bring up the console, type `un_` and hit tab (rather than enter) to see a list of them all.

The mod comes with an `autoexec.cfg` that you can edit in notepad to set your preferred options.

Hint: Setting a cvar to `0` enables original Quake 2 behaviour.  Setting it to `1` retains the remaster behaviour.


## Cvar list


### HUD

`un_damage_indicator`	0 (default): No HUD damage direction indicators, like in Quake 2.
			1	   : Remastered behaviour, damage direction appears around the crosshair.
You can also turn off Hit Markers in Options->Gameplay to avoid the red X that appears when you cause damage.


### Weapons

`un_railgun_nerf`		0 (default): Railgun damage is set to original Quake 2 levels.
			1          : Remastered behaviour, i.e. Railgun damage is reduced in single player.

`un_machinegun_smooth`	0 (default): The machinegun kicks up, like in original Quake 2.
			1	   : Remastered behaviour, i.e. no kick.

`un_blaster_buff`		0 (default): Blaster damage is reduced in single player, like in original Quake 2.
			1	   : Remastered behaviour, i.e. stronger single player blaster shots.

`un_hyperblaster_trails`	0 (default): Hyperblaster bolts do not have trails, like in original Quake 2, and Remastered.	
			1	   : Hyperblaster bolts have blaster trails, like in the Sep 4, 1997 beta of Quake 2.

`g_quick_weapon_switch`	0	   : Weapon switching time is set to original Quake 2 levels.
			1 (default): Remastered behaviour, weapons switch faster.
			     * Note that this cvar is built into the game and doesn't require the unmaster mod *

### Items

`un_barrel_delay`		0 (default): Barrels explode immediately, like in original Quake 2.
			1	   : Remastered behaviour, i.e. barrels explode on a timer unless they take a lot of damage.

`un_compass`		0 (default): You do not have a compass.
			1	   : You have a compass.
If un_compass is set to zero, you can now type `give compass` to get it. `give all` will also give you the compass.

`un_powershield_nerf`	0 (default): Powershield/screen drains at the same rate for all weapons, like in original Quake 2.
			1	   : Remastered behaviour, i.e. energy weapons drain the powershield/screen twice as fast.
You can now type `give powershield` to get it.  You might want to `give ammo` too if you don't have any cells.


### Monsters

`un_berserker_jump`	0 (default): Berserkers never jump, like in original Quake 2.
			1	   : Remastered behaviour, i.e. the Berserker can jump.
			2	   : New behaviour, see below.

New berserker jump behaviour:
If you set `un_berserker_jump` to 2, it utilises a new jumping behaviour for the berserker.  It will still act like the Remastered berserker, but with the following changes:
- You will see the berserker crouch/hunker down just before he launches his jumping attack, giving you an indication that it is coming.
- When he lands, the radius over which his slam will cause damage/kick is reduced, so you have a chance to dodge while he's in the air.

`un_flyer_smother`	0 (default): Flyers shoot from afar, like in original Quake 2.
			1	   : Remastered behaviour, i.e. flyers relentlessly advance until they smother the player in melee attacks.

`un_monster_footsteps`	0 (default): Monsters walk silently, like in original Quake 2.
			1	   : Remastered behaviour, i.e. monsters make footstep sounds.

`un_monster_die_noclip`	0 (default): Monsters remain solid during their death animations, like in original Quake 2.
			1	   : Remastered behaviour, you can walk through dying monsters.

`un_monster_sidestep`	0 (default): Monsters will not strafe to avoid grenades, like in original Quake 2.
			1	   : Remastered behaviour, i.e. monsters easily avoid grenades.

`un_monster_duck`		0 (default): Monsters will not duck projectiles, like in original Quake 2.
			1	   : Remastered behaviour, i.e. monsters can duck frequently.

`un_monster_blindfire`	0 (default): Monsters stop shooting when losing sight, like in original Quake 2.
			1	   : Remastered behaviour, i.e. monsters will fire at the corner you just ran around.

`un_monster_hyperaware`	0 (default): Monsters notice the player as they did in original Quake 2.
			1	   : Remastered behaviour, i.e. monsters can see you when you're behind them and tell each other that you're there.

`un_monster_walkjump`	0 (default): Monsters stay on the platforms/floors they spawn on, like in original Quake 2.
			1 	   : Remastered behaviour, i.e. some monsters can jump from floor to floor to chase the player.
