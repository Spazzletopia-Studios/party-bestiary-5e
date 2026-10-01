# Party Bestiary 5E

A shared bestiary for the party. Creatures the party meets in combat appear as
cards with their picture, marked **Unidentified creature** until someone
recognizes them. An **Identify** check reveals what a creature is and the facts
the player chose to recall; the party's book keeps everything it learns. 5E
compatible.

A free SpazzMods module by Spazzletopia Studios.

Install in Foundry VTT with this manifest URL:
`https://github.com/Spazzletopia-Studios/party-bestiary-5e/releases/latest/download/module.json`

Source and releases: [Party Bestiary 5E on GitHub](https://github.com/Spazzletopia-Studios/party-bestiary-5e).

## What it does

- **The book.** Open it from the dragon button on the party (group) sheet or
  on your own character sheet (after Short and Long Rest), from Token
  Controls, or with **Shift+M**. It opens on a gallery of creature cards:
  portrait, CR, how much the party knows, and how often it met them. A **New**
  tag marks a card with something you have not seen yet. Click a card and the
  book opens on that creature as a two-page spread; the arrows (or the Left and
  Right arrow keys) turn to the next card, and **All creatures** goes back. The
  right page is the creature's stat block. What the party does not know yet is
  a blank in its place; what is new to you inks in once.
- **Identify** (Token Controls, **Shift+I**, or the "Party Bestiary — Identify"
  macro in the Macros tab, folder "Party Bestiary"). **Add to hotbar** in the
  book puts that macro on your own hotbar.
  Select your character, point at a creature and press Shift+I (or target one
  creature and use the button or macro), and choose two things you want to
  recall. The check is the Study action: **Arcana** for aberrations,
  constructs, elementals, fey and monstrosities; **History** for giants and
  humanoids; **Nature** for beasts, dragons, oozes and plants; **Religion** for
  celestials, fiends and undead. The DC is **10 + half the CR**. The roll is
  hidden from the player.
  - Success: you learn what it is (name, type and CR) and your first choice.
  - Success by 5 or more: your second choice too.
  - Fail by 5 or more: you may learn something false that looks true (a world
    setting; on by default). The GM sees which facts are false, and a later
    success replaces them.
  - For an unidentified creature the dialog does not name the skill, because
    the skill would give away its type.
- **Research.** Any locked fact on a page has a Research button for a
  downtime check against the same DC.
- **Learn by fighting** (a world setting, on by default). The book also learns
  from what the players see in a fight, with no roll:
  - When the GM applies damage through dnd5e (the damage buttons on a chat
    card) and the creature resists it, takes none, or takes extra, the book
    notes that damage type.
  - Attack rolls against the creature narrow down its Armor Class. This
    follows dnd5e's own **Attack Result Visibility** (System Settings >
    Configure Visibility): "Show results & target ACs" records the exact AC,
    "Show only results" narrows a range from hits and misses ("AC 12–14"),
    and "Hide all" (dnd5e's default) teaches nothing.
  - The page writes what was seen and keeps a blank for the rest; the GM reads
    a "Seen in a fight" note and can Forget it. A new damage type, or the exact
    AC, crosses every screen like any discovery. What the party saw also
    replaces a false lead, and a bad roll never plants a false lead there.
  - Only creatures already in the book learn, and never from a hidden token,
    a blind roll or a roll only the GM saw. Damage counts only on a scene a
    player is looking at.
  - A false lead stays while the fight agrees with it; it gives way when the
    fight shows it was wrong.
- **Discoveries on every screen** (a world setting, on by default). When the
  party identifies a creature, every screen goes dark and its picture waits in
  shadow as "Unidentified creature". Then a drum hit plays, light floods the
  picture, and the name lands. New facts and fight news get a shorter banner:
  the page opens, the picture stamps down, and the facts come in one by one.
  A bar shows how much of the creature the party knows, with the new part in
  gold. News that comes during the big moment waits for it to end. A click
  closes any reveal, and the map stays usable under it.
- **Encounter log.** When a combat ends, one line records where and when, which
  creatures the players could see, how many, and how many were defeated. The GM
  can add a meeting by hand (Record meeting) or drag an actor onto the window.
- **Notes.** Party notes anyone can add to; private notes only your character
  sees; GM notes players never see.
- **GM controls.** Reveal or lock any fact, set a creature's DC (creatures with
  no CR need one), undo a result from its chat card, and remove entries.

Numbers are copied exactly from the creature, except Hit Points, which show the
stat block's **average** (a token may have rolled HP).

## Requirements

- Foundry VTT V13 or V14.
- The dnd5e system 5.3.0 or newer (built against 5.3.3 on Foundry 13 and 6.0.x
  on Foundry 14).
- A GM online: the party book is written by the GM's client.
- No other modules. It works alongside the SpazzMods Hub but does not need it.

## Settings

| Setting | Default | What it does |
|---|---|---|
| False leads | On | A fail by 5 or more plants one believable false fact |
| Show discoveries on every screen | On | The creature's picture and new facts show on every screen; identifying a creature darkens the screen for its reveal |
| Reveal sound | On | A drum hit (Foundry's own sound) when the party identifies a creature; each player can turn it down with Foundry's Interface volume |
| Log creatures from combat | On | Creatures in combat enter the book and the log by themselves |
| Learn by fighting | On | Damage types and Armor Class the players see in a fight go into the book |
| Bestiary theme (per browser) | System default | System default follows Foundry's Applications colour scheme; Dark and Light always use that look |

The two keys are in Configure Controls under Party Bestiary 5E: **Shift+M**
opens or closes the book, **Shift+I** identifies the creature under the mouse.
(Not Shift+B: dnd5e 6 opens its compendium browser with it.)

## Saving and recovery

Bestiary saves are shared across GM tabs and browsers. A busy or refused save
shows a message and keeps your note draft. Check the book before repeating a
save whose result is unknown. Refresh every client after upgrading.

Automatic fight discoveries and encounter entries wait through a busy save.
This browser keeps each waiting entry across reloads. An interrupted entry
with an uncertain result stays paused and asks the GM to check the book before
recording anything by hand. Clearing browser data removes waiting entries.
Compact save receipts remain in the world so an old browser cannot repeat a
completed action; large campaign histories will gradually increase that setting.

If a closed browser left a save guard behind, the active GM can close the other
Foundry clients, keep one open, and choose **Recover stopped clients** from the
Bestiary window's header menu. This keeps the book and saved request receipts.
It does not repeat an interrupted action. Live guards never expire on a timer.

## Known limits in 0.5.2

- Locked facts are stored in the world, so a player who opens the browser's
  developer tools can read them. The check is rolled on the player's own
  client, as every roll in Foundry is, so a changed client can fake it. This
  is a table tool, not a secret vault.
- A result card's Undo works newest first on each creature, and not after the
  GM has used Reveal or Forget on that creature.
- An unidentified card shows the token's picture, as the map does. If the
  picture's file name contains the creature's name, a player who looks at the
  file name can see it there too.
- The sheet buttons are added to the dnd5e group and character sheets; dnd5e
  shows that button row to the GM and, when players may rest, to the sheet's
  owner. With another sheet module, use Shift+M, Token Controls or the macros.
- The drum hit follows the browser's sound rules: a player who has not
  clicked in Foundry since the page loaded may not hear it.
- Learn by fighting reads damage that dnd5e itself applies and attack rolls in
  dnd5e's own chat cards. Damage typed into the HP bar by hand teaches
  nothing, and modules that replace dnd5e's attack or damage flow were not
  tested.
- New marks are kept per browser: another computer, or cleared browser data,
  starts with nothing new.
- No translations yet.

## Licence and attribution

Software: MIT (see LICENSE). Not affiliated with, endorsed by, or sponsored by
Foundry Gaming LLC. Party Bestiary 5E ships no monster data: everything it
shows is read from the creatures in your world. The skill for each creature
type follows the Study action's Areas of Knowledge table, which the dnd5e system
ships in its own rules pack.

This work includes material from the System Reference Document 5.2.1 ("SRD 5.2.1") by Wizards of the Coast LLC, available at https://www.dndbeyond.com/srd. The SRD 5.2.1 is licensed under the Creative Commons Attribution 4.0 International License, available at https://creativecommons.org/licenses/by/4.0/legalcode.
