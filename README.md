# Signature Skill

## Introduction

Just like every good hero needs some theme music, every RPG main character should have a signature skill. Locke had Steal. Edgar had those cool Tools. Setzer had the very memorable random Slot Machine thing. Signature skills is where it's at. Unfortunately, this plug-in won't help you make super sweet signature skills. You have to do that on your own. What it will do is give you that menu option on the main battle menu that allows you to execute said signature skill. It gives it a prominent place letting your players know that it's more special and unique than just your average every-day skill. If you couldn't tell already, this plugin was designed to give you that classic Final Fantasy battle menu. In this case, classic refers to FF4-9, the golden age of the series that RPG Maker itself largely resembles.

I've added a lot of extra customization like a pseudo TP-based Limit Break system, allow you to add in a couple of extra battle commands along with the ability to make some tweaks on a per actor or per class basis. While this isn't the most powerful Battle Menu customizer out there, it's easy to set up and will hopefully cover what most people want to do.


## How to Use / Parameters

### Signature Skills

This section is where you define the Signature and Limit Break Skills for any actors or classes who possess one. Actor-based Signature skills supersede any class-based ones if both would apply to the same character.

![Steal](/img/snap.png)
###### Hey look, Harold has the never been done before Steal skill as his special ability! Remove Item has been set to Yes just to show what this parameter does.

**Actor Signature Skills**
Allows you to configure actor-specific battle menus. This will override the Class Signature Skill if both would apply to the same actor.
* Actor - The actor that the Signature and/or Limit Break Skill belongs to
* Signature Skill - The Signature Skill assigned to the designated actor
* Limit Break Skill - The Limit Break skill assigned to the designated actor
* Replace Attack - Replaces the Attack command of the designated actor
* Replace Guard - Replaces the Guard command of the designated actor
* Replace Item - Replaces the Item command of the designated actor
* Remove Attack - Removes the Attack command for the designated actor
* Remove Guard - Removes the Guard command for the designated actor
* Remove Item - Removes the Item command for the designated actor

**Class Signature Skills** - These work exactly the same as Actor Signature Skills but apply to any character with the indicated class.


**Extra Commands** - This section is where you define define any extra battle menu commands that every actor can use. Say you wanted to re-create the Draw mechanic from Final Fantasy 8 that everyone loves, and when I say everyone, I literally mean everyone. You could define that here.

![Draw](/img/snap2.png)
Oh God, no! Why!

**Extra Command 1** - An extra skill that is placed in the battle menu for all characters

**Extra Command 1 Position** - The position where Extra Command 1 skill will be located. Your choices are:
* After Attack
* After Signature Skill
* After Skill Groups
* After Guard
* After Item

**Extra Command 2** - This works exactly like Extra Command 1. It will be placed after Extra Command 1 if both are assigned in the same position.


### Skill Upgrades

So Locke had steal but later on in the game, he could equip an item and upgrade it to Mug. How do you do that? That's simple too. Just define which weapons, armor or items will upgrade a Signature and/or Limit Break Skill.

![Mug](/img/snap3.png)
Harold has equipped the Thieves Gloves to turn Steal into Mug

**Weapon Upgrade Skills** - Contains a list of 3 parameters: Weapon, Original & Replace With.
* Weapon - The weapon that will upgrade a Signature and/or Limit Break Skill if it is equipped by the character
* Original - The Signature or Limit Break Skill that will be upgraded
* Replace With - The Signature or Limit Break Skill that replaces it

**Armor Upgrade Skills** - Contains a list of 3 parameters: Armor, Original & Replace With.
* Armor - The armor that will upgrade a Signature and/or Limit Break Skill if it is equipped by the character
* Original - The Signature or Limit Break Skill that will be upgraded
* Replace With - The Signature or Limit Break Skill that replaces it

**Item Upgrade Skills** - Contains a list of 3 parameters: Item, Original & Replace With.
* Item - The item that will upgrade a Signature and/or Limit Break Skill if it is in the possession of the party
* Original - The Signature or Limit Break Skill that will be upgraded
* Replace With - The Signature or Limit Break Skill that replaces it


### Chaining Upgrades

If you have a chain of upgrades that can be acquired like say Steal -> Mug -> Murder, this can easily be done by making an upgrade for an upgrade.

![Draw](/img/snap4.png)
###### Now we're talking! Why Mug someone when you can just straight-up Murder them?

Example:

If you set Steal as a Signature Skill for your Thief, sorry I mean Treasure Hunter, and have an item or equipment defined to upgrade Steal to Mug, you can also define an upgrade for Mug. Let's say that your thief has the Thieves Gloves and that is set to upgrade Steal into Mug. Later on in the game, he joins a thieve's guild and upon entry, the party gains a hidden item called Thieve's Guild Membership which is set to upgrade the Mug skill to the Murder skill. As long as your thief has the Thieve's
Gloves equipped, their Steal will be upgraded all the way to Murder. Chaining doesn't stop at one level. Murder could be upgraded as well and so on and so on.


### TP Limit Breaks
Final Fantasy 7 has those sweet Limit Breaks so, of course, this plugin has to at least somewhat recreate that kind of mechanic. It's more of a stripped down version of the Limit Break system but hopefully it's good enough for most. If this feature is activated, when a character's TP is completely filled, they will gain a Limit Break skill that replaces the indicated menu option. You are probably going to want to give each character the Trait -> Other -> Special Flag -> Preserve TP.

![Draw](/img/snap5.png)

**Activate** - Set to Yes/true if you want to use this. Set to No/false if you do not.

**Limit Break Replaces** - Select the battle command that the Limit Break replaces or None if you want it to be it's own option at the top of the battle menu. By default, this is set to replace the Attack command just like FF7 did.


### Remove Commands
This is just a way to completely get rid of unwanted battle commands that your game doesn't use.
* Remove Attack - Removes the Attack command for all characters
* Remove Guard - Removes the Guard command for all characters
* Remove Item - Removes the Item command for all characters


## Terms of Use

This plugin can be used in commercial or non-commercial projects.
Credit Frogboy in your work.


## Changelog

Version 1.0 - Initial release
Version 1.1 - Upgrade signature skills with item or equipped weapon/armor
Version 2.0 - Added Limit Break skill and a host of new customization. Replaced use of Note Tags with plugin parameters. Broke backwards compatibility with version 1 plugin.
