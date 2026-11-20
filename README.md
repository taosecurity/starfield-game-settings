# Starfield Game Settings

This page lists every setting Starfield knows about, with its built-in default value. It covers the game settings (`GMST`) you change with `setgs`, the INI settings you change with `setini` or an INI file, and the extra ones only the Creation Kit uses. Everything was read from the game itself (game version 1.16.244.0).

**View it here:** https://taosecurity.github.io/starfield-game-settings/

## Example

Say you want to know how fast time passes when you're in space.

1. Open the page and type `fCalendarTimeScaleSpace` in the search box.
2. The row shows a built-in default of 10, and a `Starfield.esm` value of 5 with the Form ID `00000859`. It is marked "Changed by Starfield.esm".

Now you know that the game you play uses 5, because the record in `Starfield.esm` replaces the built-in 10. A mod with its own record for this setting would replace the 5 in turn. To see the value in effect in your game, copy the row's `getgs fCalendarTimeScaleSpace` command and run it in the console.

## Using the console

On PC, press the **~** key (the key under Esc) to open the console, type or paste the command, and press Enter. Xbox and PlayStation have no console. Using the console turns off achievements for that save unless you use a mod that keeps them on.

## What's on the page

- The page lists 6,834 game settings: 6,626 built into `Starfield.exe`, 191 that exist only as records in `Starfield.esm`, and 17 that exist only in the DLC files. Where `Starfield.esm` has a record, its value and Form ID are shown too, and the 1,224 records that change the built-in default are marked.
- It also lists 4,923 INI settings, each with its section (`fFPWorldFOV:Camera`), and 3,774 settings only the Creation Kit defines.
- You can search, filter by kind, value type, category and "Changed by Starfield.esm", and click a console command (`getgs` / `getini`) to copy it.
- Short explanations cover the kinds of settings, how to read the names, settings worth trying, how mods change game settings, and a few fossils from earlier Bethesda games.

What's new: see the top of the [live page](https://taosecurity.github.io/starfield-game-settings/).

## Words used here

- **Game setting (GMST):** one of the engine's tuning numbers or texts, such as jump height. The game has a built-in default, and a plugin can change it with its own GMST record.
- **INI setting:** a setting read from the game's INI text files and the in-game options, such as the field of view. Plugins can't change these.
- **Plugin:** a mod's data file (`.esm`, `.esp` or `.esl`). It adds or changes records in the game.
- **Record:** one thing in a plugin, such as a weapon, a quest, a location or a setting.
- **Form ID:** a record's number, such as `00000859`. The first two digits depend on the load order.
- **Load order:** the order the game loads plugins in. When two plugins change the same record, the one loaded later wins.
- **Creation Kit (CK):** Bethesda's official editor for making Starfield mods.
- **Console:** the PC command line inside the game, opened with ~.

## How it was made

- Everything was read from the Steam copy of Starfield 1.16.244.0: `Starfield.exe`, `CreationKit.exe` and `Starfield.esm`, plus the English string file for the texts.
- The page shows only setting names, kinds and values, and no game code.
- The default is the value built into the game. INI files, the in-game options and mods can change it.
- The list is regenerated after game updates.

## Thanks

Thank you to FearTheReap3r for pointing me to his spreadsheet, the [Starfield Game Settings Database](https://www.nexusmods.com/starfield/mods/18443), which led to this page.

## Found a mistake?

Open an issue: https://github.com/taosecurity/starfield-game-settings/issues

## Credits and license

Richard Bejtlich of [Richard Presents Starfield Essentials](https://www.youtube.com/@RichardBejtlich) made this page. More Starfield tools and references are on the [Richard Presents Development Hub](https://taosecurity.github.io/).

This is an unofficial list, not made or endorsed by Bethesda. Starfield is a trademark of ZeniMax Media.

The page is a single self-contained `index.html` with no external dependencies. Its code (layout and search) is under the MIT license; see [LICENSE](LICENSE).
