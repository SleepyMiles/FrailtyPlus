## 1.2.1
- **Infection warnings in multiplayer** (new setting, on by default): the Cadaver infection's single player warnings show in multiplayer too: the air filter quality % (and "Filter inoperative!") while you stand in the plants, the high fever warnings with the fever's effect on your screen, the vines in your head sound from 60%, and the last "FOREIGN BODIES DETECTED" warning before you burst. The infection itself works as the game has it.
- New settings section **Cadaver Infection** with everything about the infection: Infected, Blooming (moved from `2. Injuries`, your values carry over) and Infection warnings in multiplayer.
- Fixed: after leaving a lobby and hosting or joining another one, the others no longer saw your healed health from FrailtyMedical / Drinkable until you restarted the game.
- Fixed: on some setups (where BepInEx' own object is removed when the game loads a scene) FrailtyMedical's healing rules weren't found.
- The extra stamina drain from leg injuries shows in EladsHUD+'s detailed stamina rate too (it already did with AdvancedCompany).

## 1.2.0

### New
- **No healing while bleeding** (with FrailtyMedical, on by default): while you have Bleeding, Laceration or Fatal Bleeding, only a Bandage, the First Aid Kit or Epinephrine can heal you. TZP, pills and other healing do nothing. Turning it off also turns off Laceration and Fatal Bleeding.
- New debuffs: **Infected**, **Blooming** (Cadaver infection) and **Paranoid**, with a % under the icon.
- **Paralysis** now jolts and shakes your view (setting `Paralysis shake`).
- UsualScrap is now a compatibility option (`UsualScrap compatibility`, off by default).

### Balance changes
- **Paralyze rework:** bee damage adds up and you roll once after you get away (level 1 / 2 / 3 by damage). No lock-ups while still stung. A teammate's **Zap Gun** gives Paralyze too.

### Icon changes
<img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/changes_1_2_0_icons.png" width="360">

- New mod icon: the glitch look with **PLUS** under Frailty.
- Redrawn icons: Laceration, Fatal Bleeding, Paralyze I-III, Paralysis.
- New icons: Infected, Blooming, Paranoid.

## 1.1.0
- Laceration and Fatal Bleeding now come with **FrailtyMedical** (its Bandage and First Aid Kit treat them). UsualScrap is no longer needed; its Bandages / Medical Kit still work if you have it.
- README: every injury icon with what it does, and new future plans.

## 1.0.1
- The injury icons show the time left above them, like TZPPlus', DrinkableSoda's and FrailtyMedical's icons.

## 1.0.0
- First release of FrailtyPlus, a fork of Frailty 1.0.0 by IntegrityChaos.
- Fall damage tiers, bleeding tiers, Laceration, Fatal Bleeding, Paralyze / Paralysis, Coil-Head concussion.
- UsualScrap Bandages and Medical Kit treat bleeding.
- Fixes: real injury chance, injuries from the damage actually taken, steam valve blindness, leg injury stamina regen, vanilla blood drops, repaired steam valves.
- Blindness / concussion no longer blur the HUD (option).
- Config synced from the host (CSync).
