# FocusFrame [BETA]
Provides [focus targeting](http://wowwiki.wikia.com/wiki/Focus_target) & frame support for vanilla World of Warcraft. (1.12.1)

If you have never used focus before, it's basically a secondary target system that keeps track of a second unit other than the currently targeted unit. Once a focus is set, you can use macros to cast spells on the focus without having to lose your current target.

The focus frame works for both friendly and enemy units.

![alt](http://i.imgur.com/Qziq2wX.jpg)

### Chat commands

Focus current target or by name:
```
/focus
/focus playername
```

Focus current mouseover target:
```
/mfocus
```

Cast spell on focus target:
```
/fcast spellname
```

Use item effect on focus target:
```
/fitem itemname
```

Target the focus target:
```
/tarfocus
```

Clear current focus:
```
/clearfocus
```

#### Options

Set frame scale: (0.2 - 2.0)
```
/foption scale 1.0
```

Toggle frame dragging:

Hold down left mouse button on focus **portrait** to move it.

If you lock the frame, then targetting focus by clicking on portrait is no longer possible. (Will fix this later)
```
/foption lock
```


### Important
When using this addon there are some limitations or caveats you should know about due to the way WoW 1.12.1 api works:

- **There's no way to distinguish between NPCs with the exact same name, so most of this addon's functionality won't work properly on mobs.**
- Mana/power for non-party member focus is updated when you or your party members target/mouseover the focus target. (Also every time you use /fcast)
- Health is updated same way as mana, but will also update when the focus target's nameplate is in range.

- Castingbar handler can't tell if focus uses downranked spells.
- Casts & buffs for focus not in party are only tracked if the focus is within 40 yards range of your character.
- Only works on English game client for now.


### Installation
[Download link.](https://github.com/wardz/FocusFrame/releases)


Unzip the downloaded file into your "WoW/Interface/AddOns/" folder, then remove "-master" (or version) suffix from the addon's folder name.


### TODO
- Add target of target frame.
- Option to fade/hide frame when focus is out of range

If you want to submit a pull request, please use the dev branch. It has the most up-to-date changes.
