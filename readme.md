# Focus and guardian

Modification of Crusader Kings 3. Requires [Elder Kings](https://www.nexusmods.com/crusaderkings3/mods/32).

Automates focus and guardian choice, for all your underage courtiers. The mod is an improvement over buddykenner's mod [Education Automation](https://catalogue.smods.ru/archives/127942).

## Technical requirements

* Crusader Kings version Crown 1.15.0.2.

* Elder Kings modification version 0.15.1.

## Features

1. A chain of events that chooses focus and then guardian is evoced monthly or by your decision.

2. Education focus choice is automatic; guardian selection if either manual or automatic, like in [buddykenner's mod](https://catalogue.smods.ru/archives/127942).

3. The event chain can be only one at any given moment (spam protection).

4. The event chain is suspended if you chose "I will think on this later" or "Don't I pay <TUTOR> to teach all children of the court?" option.

5. The event chain is restarted for another child if not suspended.

Conditions for the monthly event:

* a child of age at least 5 at your court has no guardian, is not travelling to/from education host;

* event chain is not suspended by your decision.

## Legal notice

buddykenner, thank you for releasing your wonderful mod in the public domain.

## Sample usage scenario

Suppose you want to turn nearly all your childen to your faith. Suppose further you have a 12-years old child with wrong faith and good genes in your prison. 12 years is a critical age for faith conversion; you want to start education/conversion as soon as possible.

1. You choose decision "Start Education Automation" and turn off automatic choice of guardian.

2. You release from prison the 12-year old and force her to be your courtier.

3. You do not want to wait until end of month and choose decision "Are all my children educated?".

4. The event runs for eldest child who happens to be that 12-years old. You get a dialog showing two possible guardians.

5. You take last option "I will think on this later"; choose guardian of your faith manually; select option to convert faith.

6. You again choose decision "Are all my children educated?", to enable focus-guardian loop.

## Guardian choice

Guardian choice in Focus and guardian mod is same as in Education Automation (EA) mod. I suggest that you examine [original documentation](https://catalogue.smods.ru/archives/127942).

## Focus choice

Focus is chosen automatically. No options supported. If you want to know the choice cryteria, examine code of event **edu_fix.8888** in file **focus_and_guardian/focus_and_guardian/events/edu_fix_events.txt**.

## Bugs

I want to start education at age nearly six, for instance when child is 5 years 10 month. Unfortunately there is no easy way to select child of such age. Condition 'age >= 5.8' evaluates to 'age is 5 or more'. I do not know how to properly evaluate age check without more variables and scripts on all 5-year-old courtiers; I do not want to add that many variables and scripts.

Hopefully things will be better with newer version of the game. Will return to this matter when porting the mod to the newer version, which will happen when Elder Kings supports it.

## Why change original mod Education Automation

I chose to modify the original [EA mod](https://catalogue.smods.ru/archives/127942) for the following reasons:

* EA mod only runs events once per year, not once per month; no way to force thru decision.

* EA mod does not automate focus choice.

* EA dialogs might spam: a new dialog for a next child might emerge, before I choose guardian for a previous child.

## Installation

1. Put all files except `readme.md` into `mods` directory, where you put `elder-kings-ck3.mod` file and `elder-kings-ck3` directory.

2. Activate via launcher called `dowser.exe`.

For more details on mod installation, see [wiki](https://ck3.paradoxwikis.com/Modding#Installing_mods_manually).

## Load order

"Elder Kings", then "Focus and guardian".

## List of my CK3 modifications

1. [Heal us, Mara](https://github.com/krisk0/heal_us_mara)
2. [Focus and guardian](https://github.com/krisk0/focus_and_guardian)
3. [Elder Kings fixes and tweaks](https://github.com/krisk0/ek_fixes_and_tweaks)
