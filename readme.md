# Focus and Guardian

Modification for Crusader Kings 3. Requires [Elder Kings](https://www.nexusmods.com/crusaderkings3/mods/32).

Automates focus and guardian choice for all your underage courtiers. The mod is an improvement over buddykenner's mod [Education Automation](https://catalogue.smods.ru/archives/127942).

## Technical requirements

* Crusader Kings version Crown 1.15.0.2.
* Elder Kings modification version 0.15.1.

## Features

1. A chain of events that chooses focus and then guardian is evoked monthly or by your decision.
2. Education focus choice is automatic; guardian selection if either manual or automatic, similar to [buddykenner's mod](https://catalogue.smods.ru/archives/127942).
3. Only one event chain can exist at a time (spam protection).
4. The event chain is suspended if you chose "I will think on this later" or "Don't I pay <TUTOR> to teach all children of the court?" option.
5. The event chain restarts for another child if not suspended.

Conditions for the monthly event chain activation:

* a child at your court is of age at least 5, has no guardian, is not travelling to/from education host;
* the event chain is not suspended by your decision.

## Legal notice

buddykenner, thank you for releasing your wonderful mod in the public domain.

## Sample usage scenario

Suppose you want to convert most of your childen to your faith. Suppose further you have a 12-years old child of a wrong faith and good genes in your prison. 12 years is a critical age for faith conversion; you want to start education/conversion as soon as possible.

1. You choose decision "Start Education Automation" and turn off automatic choice of guardian.
2. You release from prison the 12-year old and force her to be your courtier.
3. You are busy managing your troops and forgot to choose "Are all my children educated?" decision. Luckily the focus-guardian event chain evokes automatically at the start of the month.
4. The event is for eldest child who happens to be that 12-years old. You get a dialog showing two possible guardians.
5. If one of the two guardians if of the right faith, select them; immediately after the focus-education event chain runs for another child.
6. If neigther guardian is of the right faith, you take last option "I will think on this later"; choose guardian of your faith manually, and enable faith conversion; choose "Are all my children educated?" decision, to enable focus-guardian loop.

## Guardian choice

Guardian choice in Focus and Guardian mod is the same as in Education Automation (EA) mod. I suggest that you examine [original documentation](https://catalogue.smods.ru/archives/127942).

## Focus choice

Focus is chosen automatically. No options supported. If you want to know the choice cryteria, examine code of event **edu_fix.8888** in file **focus_and_guardian/focus_and_guardian/events/edu_fix_events.txt**.

## Bugs

### Age >= 5.8 bug

I want to start education at age nearly six, for instance when a child is 5 years 10 month. Unfortunately there is no easy way to select a child of such age. Condition 'age >= 5.8' evaluates to 'age is 5 or more'. I do not know how to properly implement age check without more variables and scripts on all 5-year-old courtiers; I do not want to add that many variables and scripts.

Hopefully things will be better with a newer version of the game. Will return to this matter when porting the mod to the newer version, which will happen when Elder Kings supports it.

### Sort by age bug

Sort by age does not work properly — not in scripts, not in user interface. When sorting children by age, first children of age 15 are selected (if any), then 14-years old, then 13, and so on. However those 15-, 14-, etc. years old, are not sorted by age. If I want to choose the eldest 15-years-old (to give them a province for instance), I need to browse through all of them and consider age in months.

If you know how to find the eldest 5-year-old in script without hurting performance, please inform me through bug report.

## Why change the original mod Education Automation

I chose to modify the original [EA mod](https://catalogue.smods.ru/archives/127942) for the following reasons:

* EA mod only runs events once per year, not once per month; no way to force thru decision.
* EA mod does not automate focus choice.
* EA dialogs might spam: new dialog for next child might emerge, before I choose guardian for previous child.

## Installation

1. Put all files except `readme.md` into `mods` directory, where you put `elder-kings-ck3.mod` file and `elder-kings-ck3` directory.

2. Activate via launcher called `dowser.exe`.

For more details on mod installation, see [wiki](https://ck3.paradoxwikis.com/Modding#Installing_mods_manually).

## Load order

"Elder Kings", then "Focus and guardian".

## List of my CK3 modifications

1. [Heal us, Mara](https://github.com/krisk0/heal_us_mara)
2. [Focus and Guardian](https://github.com/krisk0/focus_and_guardian)
3. [Elder Kings fixes and tweaks](https://github.com/krisk0/ek_fixes_and_tweaks)
