# Welcome to Annosz's Stardew Valley modding guide

Stardew Valley is a fantastic game. The tranquil, simple - yet in the same time, extremely deep - contryside absorbed me at the moment I set foot in Pelican Town. The farming help me in my final years of university when *"I'd lost sight of what mattered most in the life..."* and after the multiplayer update, I even managed to find new friends in the game.

As a programmer and serial modder, after a few playthrough I naturally started to search for mods, to deepen this experience even more. I joyfully discovered that the modding community for this game is exremel active, the tools are consistently kept up-to-date with the latest patches and even inexperienced modders are encouraged to start their own projects and enrich the game.

This guide is ment to be a help for those, who are not really technically savy or does not have the time to browse wiki sites, forums or Discord to find and compare the available mods, but want to use them and have as much fun with Stardew Valley as possible - just like me.

* Table of contents
{:toc}

## How to use this guide

This guide's greatest advantage is that it's written by me.

Also, this guide's greatest weaknes is that its written by *me*.

This means, that this guide - even if it tries to be a comprehensive, objective guide - will contain some of my opinion about the mods mentioned. I will feature very few mod as mandatory (mainly in the *Before you start modding* section, which are really **mandatory**), so you don't have to worry that I will change your game experience in a way you don't want to. However, I will tag a lot of mods as **not recommended**, because they are simply unbalanced or ruin the immersion (for me). When I say you should not install a mod, I will always mark my reason too, and you are free to second-guess it.

From now on, I will use the following marks:
- :heart:: Mods that good that they should be in the original game
- :green_heart:: A good mod which deserves to be in your game
- :yellow_heart:: This mod has it's drawback (most likely not compatible with a better mod or slightly unbalanced), and you should decide whether you want to cope with these or not
- :broken_heart: I'm against installing this mod (most likely it's unbalanced, ruines immersion or crashes the game)

A few other things you should keep in mind while you read this guide:
- I mainly wrote this guide with the intention to help my friends, who play the game but are not *expert* modders. This means I try to give exact instructions on how to install the mods, how to use the tools and how to check for errors. If you are more experienced, maybe you will read a lot of boring information (mainly because Stardew Valley is generally easy to mod).
- This mod list is **not complete**. You will always found other mods on the internet, and you are free to go and look for anything that satisfies your special interest. I tipically do not feature mods, that are targeted for a very small audience(?), such as the mod that [lets you ride Chocobos](https://www.nexusmods.com/stardewvalley/mods/2613 "Chokobomod") from Final Fantasy, or the one that replaces every marriable male character to [girls with huge breasts](https://www.nexusmods.com/stardewvalley/mods/474 "StardewValley_Girl-byAdarin"). You have to search for theese yourself.
- No guide can always be completely up-to-date. To help this, I will talk a lot in the section *Finishing up* about typical errors, messages and their solutions, hoping, that when the game updates or the mods change version you will still be able to fix the majority of problems alone.
- At many places you will be presented with a collection of mods which are not compatible with each other. In these cases, you will have to make a decision which one yo want to install - it only depends on your taste.

## Resources
All of the knowledge which is presented here is the product of many-many Stardew Valley players and modders. My only purpose was to make it available in one place, but I can't argue that the recognition should go to those who originally created the content.

Here are the main information sources I used. These pages can be useful for you after you finished this guide, and want to go on to search for other mods, or you want to became a modder yourself.
- [Stardew Valley Nexus](https://www.nexusmods.com/stardewvalley): This is your main source of mods: it contains thousands of mods with screenshots, descriptions, files and installation instructions.
- [SMAPI Mods](https://mods.smapi.io/): On SMAPI's website you can find another collection of mods, focusing on SMAPI compatibility (you can read about it in the *SMAPI* section). This table is a very good synopsis of mods, with short descriptions and sources. It is even worth checking compatibility here if you install mods from somewhere else, as if it has some problems you can usually find a link to a patch.
- [Stardew Valley Wiki - Modding](https://stardewvalleywiki.com/Modding:Index): The Stardew Valley Wiki contains a detailed section on modding. It contains pages which can help you install SMAPI or different mods, and has a guide for modders too. I will reference these pages in my guide too, as they are well-written and it's not worth copy-pasting the same information here.
- [Stardew Valley Wiki - Alternatives using Content Partcher](https://stardewvalleywiki.com/Modding:Using_XNB_mods#Alternatives_using_Content_Patcher): Another page you can check while you are installing mods online. It is a good collection of mods that have been rewritten from XNB to Content Patcher - more on this topic on the *Content Patcher* section.
- [Stardew Valley Forum - Mods](https://community.playstarbound.com/forums/mods.215/): You can always find resources and help on the Stardew Valley Forum, which has a separate section for modding. Don't worry if you don't usally use forums, I'm also going to link everything here what is needed at the appropriate sections.
- [Stardew Valley Discord](https://discordapp.com/invite/stardewvalley): I strongly recommend joining the Stardew Valley Discord, because it is a very lively community, and they can help you a lot with modding. If you are not familiary with Discord, it is a chat app for gamers, and in this Stardew Valley server you can find and talk to other players who are active part of the community.

# Before you start modding

To install mods, you first need to make some preparations. In the whole guide these will be the only steps, that are mandatory (or at least SMAPI and Content Patcher), and you have to make these **before installing any other mods**.

First of all: **you should always update your game and mods to the current version** - or not. The main thing is that you do this consistently, and your versions match: if you have Steam for example, then it will always update your game for you, and you should keep your mods in sync with it (following the steps in the *Configure, update or delete mods* sections, preferably together with *Mod Update Menu*).

If you don't want to update your mods, the you have to make sure that you disable the game update for Stardew Valley in Steam's or GoG's options. However, in this case if you want to install a newer mod, you will most likely won't be able to use it because your game version will be older than it's minimal requirement :( This option is only recommended, if you are really-really sure that you want to freeze the game to one version and only use that.

## SMAPI
**SMAPI (Stardew Modding API)** is the main foundation we have to build on. This is the API (Application Programming Interface) that let's modders to change the game, and write extensions to it - which means basically *every* mod needs it. It also provides update checks and compatibility checks between mods: you will see warnings when you start the game which let you know that you have to download the latest version of a mod. It also provides error check, so a misfuncioning mod won't crash your whole game or corrupt you save if you load it with SMAPI - so yeah, it is pretty important.

There are a lot of places where you can download SMAPI, but I suggest [smapi.io](https://smapi.io/), where you will always find the latest version. I don't want to give detailed information about installing it (although this will probaby be the hardest thing to install in the guide), because there are a lot of resources for it: I suggest to follow the SMAPI install guide on Stardew Valley Wiki, which has instructions fow [Windows](https://stardewvalleywiki.com/Modding:Installing_SMAPI_on_Windows "Modding:Installing SMAPI on Windows") (there is even an [unofficial video guide](https://www.youtube.com/watch?v=9ULXeC9CL0c "How to Install SMAPI + Mods for Stardew Valley (PC)") from MollyPop
), [Mac](https://stardewvalleywiki.com/Modding:Installing_SMAPI_on_Mac "Modding:Installing SMAPI on Mac") and [Linux](https://stardewvalleywiki.com/Modding:Installing_SMAPI_on_Linux "Modding:Installing SMAPI on Linux") too.

It is important to install SMAPI correctly: if you use the Steam version of the game, modify the launch options like written in the guide, otherwise you will not be able to earn achievements.

There are also two mods that are instantly included in SMAPI, and can be quite helpful:
- :heart: SaveBackup: SMAPI automatically creates a daily backup of your saves and keeps ten backups, in case something goes wrong.
- :heart: ConsoleCommands: In the SMAPI console which opens when you start the app, you can use various commands/cheats. These mainly have testing/modding development purposes, so I advise you don't use it for making your game easier. A full list of Console Commands can be found at the [Stardew Valley Wiki](https://stardewvalleywiki.com/Modding:Debug_commands "Modding:Debug commands").

## ~~StarDew Valley ModManager~~
**StarDew Valley Mod Manager (SDVMM)** was a very useful tool when it was regularly updated. I mainly feature it here to warn everyone that today it throws errors for almost anything, so it's not worth downloading. It's main features (updating SMAPI, mods, enabling and disabling them, launching the game) can be all done with other (or without) tools.

The ModManager was originally available on the [Nexus](https://www.nexusmods.com/stardewvalley/mods/21?tab=posts "StarDev Valley ModManager"), where an installation guide video is available, and you could download the latest version from the [Github page](https://github.com/yuukiw/StardewValleyMM/releases "StarDev Valley ModManager"), but again, I don't recommend it.

## How to install the mods
After you install SMAPI, installing mods will be as easy as copy-pasting folders into the game's directory (SDVMM would make it easier with a graphic interface, but it does not work).

Generally, there are two types of mods:
- SMAPI mods, which can be installed by copying them into the *Mods* folder in your Stardew Valley install location. On [Stardew Valley Wiki](https://stardewvalleywiki.com/Modding:Player_Guide/Getting_Started#Find_your_game_folder "Find your game folder") there is a little help to find this folder. Most likely you download your mods in a .zip file, wich you have to unzip, then copy the **whole folder** into the *Mods* folder (there is also an example for this on the [Wiki](https://stardewvalleywiki.com/Modding:Player_Guide/Getting_Started#Install_mods).
- XNB mods: In the old times, to install specific mods, you had to edit game files - for every mod, there was a different file in a different location, with the risk of corrupting your whole game. These are mainly the mods that change images in the game - for example if you want to change the portrait of a villager, you had to delete the previous and insert the new.
You can strill find these mods on the internet, but you should **not use them**. For almost all of them there is an alternate mod of installation, which you will read more about in the *Content Patcher* section.

### Configure, update or delete mods
You can also find detailed information about making changes to mods on the [Wiki](https://stardewvalleywiki.com/Modding:Player_Guide/Getting_Started#Configure_mods), but the most important thing are:
- There are mods you can configure. Usually this information is signalled on the mod page, an it lists the options you can choose from. You can use these options by opening the *config.json* file in the mod's folder with a text editor (like notepad), and changing the values you want to modify.
- Updating is as easy as installing mods: just replace the old files with the new ones (and keep your modifications on the *config.json*, if you made any).
- Deleting a mod is done by removing its folder from the *Mods* folder.

## Content Patcher
In the *How to install the mods* section I talked about the two types of mods, and how dangerous was it to install XNBs. This is what changed with **Content Patcher**: it makes it possible to install these by simply copying them to the game folder, checking for updates or removing them without editing the game files.

You have to install [Content Packer](https://www.nexusmods.com/stardewvalley/mods/1915) **after SMAPI**, similary to installing any mods: extracting it to the *Mods* folder (discussed in the *How to install the mods* section).

After this when you see a mod, make sure that you do not download an XNB version but the SMAPI one. Most of the original mods now have unofficial SMAPI replacements, which can be found on [this forum](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/). A list that makes it easyier to search the mods also [exists here](https://stardewvalleywiki.com/Modding:Using_XNB_mods#Alternatives_using_Content_Patcher).

For example: when I found the original [Seasonal Buildings and flowers](https://www.nexusmods.com/stardewvalley/mods/891) mod, I saw a bunch of instructions on how to install it (and it's not even a real XNB mod, it already has some SMAPI support!). But in the comments, I foun the link to the [Content Patcher version](https://www.nexusmods.com/stardewvalley/mods/3691), and when I used that it was enough to only download the .zip and extract it to the *Mods* folder as with every other mod. Of course in this guide I always write the CP links, not the XNB ones, but if you want to install mods on your own, watch out for this.

## Mod Update Menu
The [Mod Update Menu](https://www.nexusmods.com/stardewvalley/mods/2536) extends the Main Menu of the game with an extra window where you can find informations about your mods. It warns you if any of them has available updates (or if your SMAPI is not up-to-date), which is very useful - this way you can prevent errors caused by incompatible versions. It even shows the download link, so you can instantly go to the Nexus and download the new version.

The only problem is that it only knows Nexus mods. This means you should always download your mods from here - but there are always some mods you find on the forums (for example Content Patcher replacements) which show up as errors. Apart from this, they only mean a minor inconvinience: they will simply be left out of version checkings, and have a very annoying red color in the menu.

# Installing the mods

## 1. Graphic mods

<dl><dt>Choose one setting to your liking</dt></dl>

<dl><dt>    -> If you fancy a little Victorian look:</dt></dl>

- :green_heart: [Eemie's Seasonal Victorian Buildings - Content Patcher](https://www.nexusmods.com/stardewvalley/mods/3691): New Vistorian buildings, if you are into this stuff (you are playing Stardew Valley, so I guess you must be into beautiful stuff). Use this Content Patcher version instead of any old one you find.
- :yellow_heart: [Obelisk Overhaul Inspired By Eemi Seasonal Victorian](https://www.nexusmods.com/stardewvalley/mods/3198): Replaces the obelisks to match the previously installed victorian mod. The only drawback is that if you install *Desert Obelisk Mod* or *Deep Woods* you have to manually replace the corresponding images in every season. You can try to create hand-made XNB mods for these too if you feel like it, but otherwise I suggest to skip this mod, as I think the default totems do not look that bad in the Victorian setting to worth the trouble.
- :green_heart: [SMAPI Seasonal Victoraian Buildings and Flowers](https://www.nexusmods.com/stardewvalley/mods/2050): A very nice recolor, that does well with the *Seasonal Victoraian Buildings and Flowers*. Use this Content Patcher version instead of any old one you find. After you start the game once and the config files are generated, you can edit the options for recolor, as written in the mod description.
  - This mod already contains :green_heart: [Ali's Flower Grass](https://www.nexusmods.com/stardewvalley/mods/2051): If you'd like a vivid Stardew Valley, this is the mod for you. Goes along perfectly with the Victorian style - you just have to set "UseEemieGrass": "false" (othervise it uses another grass mode) and "AliGrass": "Eemie" (or anything you like) in the config file.

<dl><dt>    -> If you are more into medieval stuff:</dt></dl>

- ...

<dl><dt>    -> Other (choose one if you haven't choose from the previous categories):</dt></dl>

- ...

___

<dl><dt>Choose one interior mod:</dt></dl>

- :green_heart: [Elegant Victorian Interior](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-8#post-3275117) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/1074 "Elegant Victorian Interior") page): Make sure to download the SMAPI mod from the provided link (don't let the name deceive you, *Mi's Victorian Furniture* is inspired by Eemie's work).
- :green_heart: [Classy new interior](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-66#post-3306821) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/854 "Classy new interior") page): Make sure to download the SMAPI mod from the provided link.
- :green_heart: [Dark brown and cream colored furniture](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-54#post-3303093) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/2190 "Dark brown and cream colored furniture") page): Make sure to download the SMAPI mod from the provided link.

___

- :heart: [Ali's Flower Grass](https://www.nexusmods.com/stardewvalley/mods/2051): If you haven't installed it with *SMAPI Seasonal Victoraian Buildings and Flowers*, I suggest you go for it: it adds beautiful grass to the game, which is configurable from the config file.
- :green_heart: [Hojichas' Walls and Floors (Content Patcher)](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-23#post-3285313) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/912 "Hojichas' Walls and Floors (Content Patcher)") page): Make sure to download the SMAPI mod from the provided link. This mod is essential to make your house look like on previously installed mod's pictures, because almos all of them has matching wall styles in this.
- :heart: [Elle's Barn Animal Replacements](https://www.nexusmods.com/stardewvalley/mods/1960): When you install it, you have to select a style for each animal you want to replace. For reference, see the images on the Nexus page, and copy only the one folder that you selected into the *Mods* folder of your game.
- :heart: [Elle's Coop Animal Replacements](https://www.nexusmods.com/stardewvalley/mods/1962): When you install it, you have to select a style for each animal you want to replace. For reference, see the images on the Nexus page, and copy only the one folder that you selected into the *Mods* folder of your game.
- :heart: [Elle's Horse Replacements](https://www.nexusmods.com/stardewvalley/mods/1963): When you install it, you have to select a style for each animal you want to replace. For reference, see the images on the Nexus page, and copy only the one folder that you selected into the *Mods* folder of your game.
- :heart: [Elle's Critter and Butterfly Replacements (Content Patcher)](https://www.nexusmods.com/stardewvalley/mods/1965): Recolors butterflies, critters, etc. You don't have to choose from different versions, you can install the whole pack.
- :green_heart: [Elle's Dirt and Cliff Recolor (Content Patcher)](https://www.nexusmods.com/stardewvalley/mods/1966): Recolor for dirt and cliffs.
- :green_heart: [Bathhouse Hot Spring - Content Patcher](https://www.nexusmods.com/stardewvalley/mods/3110): A totally new style for the bathhouse.
- :green_heart: [Darker wood and gold craftables](https://www.nexusmods.com/stardewvalley/mods/687): Gives a darker color to wooden craftables.
- :green_heart: [Animal Crossing Digspot - Worm Replacement](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/#post-3259191) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/18 "Animal Crossing Digspot - Worm Replacement") page): Slightly better visible than worms, and gives a nostalgic feeling if you played Animal Crossing.

## 2. Map extensions
- :green_heart: [DeepWoods](https://www.nexusmods.com/stardewvalley/mods/2571) Adds a new well-designed, mine-like part to the forest. It is a good addition to the game, has a nice balance and difficulty, and a ton of interesting encounters and events. It is compatible with a lot of other mods, except for the very similar:
- :yellow_heart: [Even More Secret Woods](https://www.nexusmods.com/stardewvalley/mods/2364) Another mod that extends the forest. This one is more unbalanced (basically just ads more hardwood without a challenge), less detailed, not updated and if you want to add it to an existing save, you have to use *Entoarox Framework* as explained in the description. It also has compatibility issues with *DeepWoods*, so I recommend picking the previous one. If you still want to use both of them, you can find help in the description of *DeepWoods* and a patch among the downloadable files.
- :green_heart: [Bathroom after 2nd Houseupgrade](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-20#post-3283861) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/299 "Bathroom after 2nd Houseupgrade") page): Adds a bathroom to your house, that funcions exactly as the bathhouse. *Maybe* a little unbalanced, but I think that at that part of the game when you have access to the 2nd house upgrade you usally have enough energy for a day and time is a biggern concern during the daily chores.

## 3. User Interface

## 4. Character creation

## 5. Villagers

## 6. Gameplay
- :green_heart: [Desert Obelisk](https://www.nexusmods.com/stardewvalley/mods/2021) A simple mod that ads a Desert Obelisk to the game. Quite useful and balanced.

## 7. Other mods

# Finishing up

