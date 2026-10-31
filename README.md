# FrailtyPlus

[Frailty](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Frailty/) by **IntegrityChaos**, rebuilt for `V81` and expanded. Getting hurt can leave you with injuries: broken legs, bleeding, concussions and more, each with its own icon and time left.

**Replaces Frailty.** Don't install both. FrailtyPlus keeps Frailty's plugin ID, so mods made for Frailty still work with it.

> **Made to go with [TZPPlus](https://thunderstore.io/c/lethal-company/p/SleepyMiles/TZPPlus/), [FrailtyMedical](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyMedical/), [Drinkable](https://thunderstore.io/c/lethal-company/p/SleepyMiles/Drinkable/) and [EladsHUD+](https://thunderstore.io/c/lethal-company/p/SleepyMiles/EladsHUDPlus/).** EladsHUD+ shows every injury under your health bar with the `time left`, and you can point at an icon to see what it does. TZPPlus heals leg and arm injuries faster while you inhale. FrailtyMedical gives you the bandages, kits and pills to treat everything.

<img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/frailty_vanilla.gif" width="360"> <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/frailty_eladshud.gif" width="360">

*Left: the vanilla HUD. Right: with EladsHUD+.*

---

## Injuries

<details>
<summary>🦴 Fall damage</summary>

The bigger the fall, the worse the injury. It uses the damage you actually took, so anything that lowers fall damage (TZPPlus, perks) also lowers the injury.

| Damage taken | Fractured Leg | Broken Leg |
|---|---|---|
| below 10 | - | - |
| 10-29 | 10% / 20 s | - |
| 30-49 | 15% / 40 s | - |
| 50-79 | 25% / 60 s | 10% / 90 s |
| 80+ | 30% / 120 s | 25% / 150 s |

- A second Fractured Leg turns into a Broken Leg. Leg injuries stack their time.
- Fractured / Broken Legs make sprinting drain your stamina faster.

</details>

<details>
<summary>🩸 Bleeding, Laceration and Fatal Bleeding</summary>

- **Mauling** (Thumper, Bunker Spider, Hoarding Bug, Spore Lizard, Cadaver) and the **Baboon Hawk**: the more damage (hits within 3 s add up), the higher the chance and the longer you bleed.
- **Stabbing** (Butler, Mask Hornets, Giant Sapsucker) and **Scratching**: same, but a bit more likely and longer.
- **Gunshots** always bleed. The Fan and Snipping can.
- **Bleeding**: no health regen and a blood trail. With FrailtyMedical you can't heal at all while you bleed, except with a Bandage, the First Aid Kit or Epinephrine (TZP, pills and other healing do nothing).
- With **[FrailtyMedical](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyMedical/)** installed, big hits can cause a **Laceration** instead. Treat it within 20 s with a Bandage or the First Aid Kit, or it becomes **Fatal Bleeding**: you keep losing health until it stops, and it can kill you.
- FrailtyMedical's **Bandage** stops Bleeding and Laceration and slows Fatal Bleeding down to Bleeding; its **First Aid Kit** treats every kind of bleeding.
- `Forgiving Fatal Bleeding` option: a slow drain that won't kill a healthy player.

</details>

<details>
<summary>⚡ Paralyze (Circuit Bees)</summary>

- The bee damage you take adds up. **2 s after you get away**, one roll on the total:

| Bee damage before getting away | Paralyze |
|---|---|
| 10-29 | 40%, level 1 |
| 30-59 | 75%, level 2 |
| 60+ | always, level 3 |

- A teammate's **Zap Gun** on you for 1 s or more gives Paralyze level 1.
- While Paralyzed, every second it may lock you up with **Paralysis** for 1-2 s: you can't move or jump, your camera turns slowly and your view jolts and shakes. Higher levels lock you up more often. No lock-ups while the bees are still on you.

</details>

<details>
<summary>🦠 Infection and paranoia</summary>

These read the game's own state, so they show what is really happening to you.

- **Infected**: Cadaver spores. Shows once the game's infection reaches `60%`, with the % under the icon. The ship's shower or weed killer clears it (the % pulses while it goes down).
- **Blooming**: the burst stage. The % counts up, and at `100%` a Cadaver Bloom bursts out of you. The game can't cure it any more.
- **Paranoid**: your paranoia (the game's insanity) is at `75%` or more, where the creepy sounds start. Stay near your crew to bring it down.
- **Infection warnings in multiplayer** (on by default, `Infection warnings in multiplayer`): the game only tells you about the infection when you play alone. With this on you get the same in multiplayer: the air filter quality % while you stand in the plants, the high fever warnings with the fever's effect on your screen, the vines in your head sound, and the last warning before you burst.

</details>

<details>
<summary>💫 Concussion, broken arms, blindness</summary>

- Hits, blasts, kicks, car crashes (inertia) and **crushing** (Old Bird stomp, Cruiser) can concuss you and fracture / break an arm (heavy items slip out of your hands).
- A **Coil-Head** hit always concusses you for a few seconds.
- Burst **steam valves** can blind you (not once they are repaired).
- Blindness and concussion only affect the game view. Your HUD stays readable (`Keep HUD clear`).

</details>

<details>
<summary>🔧 Fixes over Frailty 1.0.0</summary>

- The injury chance now works: before, the first matching hit from full health always gave the injury.
- Injuries are rolled after the damage, from the damage you actually took. A hit that was blocked does nothing.
- Steam valves rolled blindness every frame (almost instant). Now once per second, and not while already blind.
- Leg injuries no longer double your stamina regen.
- Vanilla's critical-injury blood trail works again.
- No more "Damage type isn't supported yet" log spam.

</details>

---

## Buffs & debuffs

- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_fractured_leg.png" width="40"> `Fractured Leg` (debuff): Sprinting drains your stamina faster. A second one turns into a Broken Leg.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_broken_leg.png" width="40"> `Broken Leg` (debuff): Sprinting drains your stamina much faster.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_fractured_arm.png" width="40"> `Fractured Arm` (debuff): You can't hold heavy items (over 25 lb): they slip out of your hands.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_broken_arm.png" width="40"> `Broken Arm` (debuff): You can't hold heavy items (over 15 lb): they slip out of your hands.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_bleeding.png" width="40"> `Bleeding` (debuff): No health regeneration, and you leave a blood trail. With FrailtyMedical, only a Bandage, the First Aid Kit or Epinephrine can heal you.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_laceration.png" width="40"> `Laceration` (debuff): A deep wound. Treat it in time with a Bandage or the First Aid Kit (FrailtyMedical), or it becomes Fatal Bleeding.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_fatal_bleeding.png" width="40"> `Fatal Bleeding` (debuff): You keep losing health until it stops, and it can kill you. A Bandage slows it down to Bleeding.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_concussed.png" width="40"> `Concussed` (debuff): Your view is blurred (only the game view, your HUD stays readable).
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_blindness.png" width="40"> `Blinded` (debuff): Steam in your eyes: you can barely see (only the game view).
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_paralyze.png" width="40"> `Paralyze` (debuff): Circuit Bee stings or a Zap Gun. Every second it may lock you up with Paralysis.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_paralyze2.png" width="40"> `Paralyze II` (debuff): More stings: Paralysis comes more often.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_paralyze3.png" width="40"> `Paralyze III` (debuff): The most stings: Paralysis comes the most often.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_paralysis.png" width="40"> `Paralysis` (debuff): Locked up for 1-2 s: you can't move or jump, your camera turns slowly and your view shakes.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_infected.png" width="40"> `Infected` (debuff): Cadaver spores are growing inside you. The % is the infection.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_blooming.png" width="40"> `Blooming` (debuff): The spores are bursting out. At 100% a Cadaver Bloom bursts out of you.
- <img src="https://raw.githubusercontent.com/SleepyMiles/FrailtyPlus/main/images/icon_paranoid.png" width="40"> `Paranoid` (debuff): You're getting paranoid. Stay near your crew to calm down.

---

## Configuration

`BepInEx/config/Chaos.Frailty.cfg`, or in-game with **LethalConfig**. Everything except `1. Effects` is **synced from the host**.

| Section | What |
|---|---|
| 1. Effects | Keep HUD clear, Fatal Bleeding red flash, Paralysis shake, infection warnings in multiplayer (your own settings) |
| 2. Injuries | turn each injury on / off (Infected, Blooming, Paranoid too) |
| 3. Chances | arm, bleeding, blindness, concussion, Coil-Head |
| 4. Times | how long each one lasts |
| 5. Fall damage | the 4 tiers, Fracture to Broken conversion, max leg injury time |
| 6. Bleeding | the 4 tiers, hit window, Stabbing bonus |
| 7. Laceration and Fatal Bleeding | on / off (also no healing while bleeding), UsualScrap compatibility, times, damage, Forgiving mode |
| 8. Paralyze | escape delay, the 3 levels, Zap Gun, times, camera speed |
| 9. Other | steam roll interval, AdvancedCompany perks |

---

## Compatibility

- **[EladsHUD+](https://thunderstore.io/c/lethal-company/p/SleepyMiles/EladsHUDPlus/)**: shows all injuries (Paralyze with its level) with time left and tooltips.
- **[TZPPlus](https://thunderstore.io/c/lethal-company/p/SleepyMiles/TZPPlus/)**: inhaling heals leg / arm injuries faster; its damage reduction also lowers injuries.
- **UsualScrap** (optional): turn on `UsualScrap compatibility` (off by default) and its Bandages / Medical Kit treat bleeding too.
- **AdvancedCompany** (SleepyMiles v.81 version): Sprint endurance / Bodybuilder also reduce the leg injury drain.
- **[Drinkable](https://thunderstore.io/c/lethal-company/p/SleepyMiles/Drinkable/)**: drinks and pills that cure or shorten injuries.
- **[FrailtyMedical](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyMedical/)** (Beta): Bandage, First Aid Kit, Morphine, Epinephrine, Painkillers and Antibiotics that treat every injury. Made for FrailtyPlus (needs it).

## Play them together

These mods are made by **SleepyMiles** to work as one set. They share one row of buff / debuff icons (or EladsHUD+'s status row) and one **CONSUMABLES** store section, and they know about each other's effects. Each one also works on its own (FrailtyMedical needs FrailtyPlus).

| Mod | What it adds |
|---|---|
| [TZPPlus](https://thunderstore.io/c/lethal-company/p/SleepyMiles/TZPPlus/) | The TZP heals you, shows its gas, builds up damage reduction (fall damage too). Too much gives a Lethal Dose. |
| **FrailtyPlus** (this mod) | Injuries: broken / fractured legs and arms, bleeding, concussions, Paralyze. A rebuilt Frailty. |
| [FrailtyMedical](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyMedical/) | *Beta.* Bandage, First Aid Kit, Morphine (revive a teammate), Epinephrine, Painkillers and Antibiotics to treat them. |
| [Drinkable](https://thunderstore.io/c/lethal-company/p/SleepyMiles/Drinkable/) | Drink the Red soda, 19 new drinks with their own buffs, the Soda Machine and the Drink Machine. |
| [EladsHUD+](https://thunderstore.io/c/lethal-company/p/SleepyMiles/EladsHUDPlus/) | Elad's HUD for V81, with a status row that shows every buff, debuff and injury from all of these with the `time left`. |

## Future plans

- **Icons:** a more polished version of every buff / debuff icon.
- **Descriptions:** clearer buff / debuff descriptions.

## Original Frailty

FrailtyPlus is a fork of [Frailty](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Frailty/) by **IntegrityChaos** (formerly "Player Conditions" from [Diversity](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Diversity/)). All the credit for the original idea, icons and effects goes to them. If you like it, support the original creator:

- [Discord](https://discord.gg/4APzjc8fNW): IntegrityChaos' server.
- [Patreon](https://www.patreon.com/IntegrityChaos): support their work.

Please report bugs in FrailtyPlus to us (SleepyMiles), not to IntegrityChaos.

## Credits

- [Frailty](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Frailty/) by **IntegrityChaos**: the original mod, its icons and effects. Licensed CC BY-NC-SA 4.0.

## License

CC BY-NC-SA 4.0, the same as Frailty (see `LICENSE`). Non-commercial use only.
