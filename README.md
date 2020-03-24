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
- Deleting a mod is done by removing it's folder from the *Mods* folder.

## Content Patcher
In the *How to install the mods* section I talked about the two types of mods, and how dangerous it was to install XNBs. This changed with **Content Patcher**: it makes possible to install XNBs by simply copying them to the game folder, checking for updates or removing them without editing the game files.

You have to install [Content Packer](https://www.nexusmods.com/stardewvalley/mods/1915) **after SMAPI**, similarly to installing any mods: extracting it to the *Mods* folder (discussed in the *How to install the mods* section).

After this when you see a mod, make sure that you do not download an XNB version but the SMAPI one. Most of the original mods now have unofficial SMAPI replacements, which can be found on [this forum](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/). A list that makes it easyier to search the mods also [exists here](https://stardewvalleywiki.com/Modding:Using_XNB_mods#Alternatives_using_Content_Patcher).

For example: when I found the original [Seasonal Buildings and flowers](https://www.nexusmods.com/stardewvalley/mods/891) mod, I saw a bunch of instructions on how to install it (and it's not even a real XNB mod, it already has some SMAPI support!). But in the comments, I foun the link to the [Content Patcher version](https://www.nexusmods.com/stardewvalley/mods/3691), and when I used that it was enough to only download the .zip and extract it to the *Mods* folder as with every other mod. Of course in this guide I always write the CP links, not the XNB ones, but if you want to install mods on your own, watch out for this.

## Mod Update Menu
The [Mod Update Menu](https://www.nexusmods.com/stardewvalley/mods/2536) extends the Main Menu of the game with an extra window where you can find informations about your mods. It warns you if any of them has available updates (or if your SMAPI is not up-to-date), which is very useful - this way you can prevent errors caused by incompatible versions. It even shows the download link, so you can instantly go to the Nexus and download the new version.

The only problem is that it only knows Nexus mods. This means you should always download your mods from here - but there are always some mods you find on the forums (for example Content Patcher replacements) which show up as errors. Apart from this, they only mean a minor inconvinience: they will simply be left out of version checkings, and have a very annoying red color in the menu.

## Minor mods required by other mods
There are a few mods that do not change the gameplay, but extend modding possibilities (for example enhance SMAPI), and are required by other mods. This means you have to install these before you can use the mods depending on them.

Of course you can choose to only install one if you want to use any mods that requires it, but I think it's easier to just intall them now. They do not change the game by any means, and they are required in mods that are present in this guide, so you can spare some debugging and headache if you just do it now.

- :heart: [PyTK - Platonymous Toolkit](https://www.nexusmods.com/stardewvalley/mods/1726): Required by a lot of other mods, eg. *Climates of Ferngill* and *Mermaid Island*
- :heart: [Json Assets](https://www.nexusmods.com/stardewvalley/mods/1720): Required by a lot of other mods, eg. *Poppi's Kawaii Valley* and *Line Sprinklers*
- :heart: [Farm Type Manager](https://www.nexusmods.com/stardewvalley/mods/3231): Required by a moderate ammount of other mods, eg. *Better Quarry Redux* and *Stardew Valley Expanded*
- :heart: [Producer Framework Mod](https://www.nexusmods.com/stardewvalley/mods/4970): Required by a moderate ammount of other mods, eg. *Coffee Maker*
  - :yellow_heart: [Custom Farming Redux](https://www.nexusmods.com/stardewvalley/mods/991): This is technically an earlier variation of *Producer Framework Mod*. Most mods that use CFR has been updated to PFM, and the ones that not are most likely abandoned and broken. I suggest you to only install this mod if it's specifically required for one of your mods, otherwise feel free to skip it.
- :heart: [SpaceCore](https://www.nexusmods.com/stardewvalley/mods/1348): Required by a few other mods, eg. *Cooking Skill* and *Artisan Valley*
- :heart: [Stardust Core](https://www.nexusmods.com/stardewvalley/mods/2341): Required by a few other mods, eg. *Happy Birthday*
- :heart: [Stardew Hack](https://www.nexusmods.com/stardewvalley/mods/3213): Required by a few other mods, eg. *Bigger Backpack* and *Yet Another Harvest With Scythe Mod*

# Installing the mods

## 1. Graphic mods

<dl><dt>Choose one setting to your liking</dt></dl>

<dl><dt>    -> If you fancy a little Victorian look:</dt></dl>

- :green_heart: [Eemie's Seasonal Victorian Buildings - Content Patcher](https://www.nexusmods.com/stardewvalley/mods/3691): New Vistorian buildings, if you are into this stuff (you are playing Stardew Valley, so I guess you must be into beautiful stuff). Use this Content Patcher version instead of any old one you find.
- :yellow_heart: [Obelisk Overhaul Inspired By Eemi Seasonal Victorian](https://www.nexusmods.com/stardewvalley/mods/3198): Replaces the obelisks to match the previously installed victorian mod. The only drawback is that if you install *Desert Obelisk Mod* or *Deep Woods* you have to manually replace the corresponding images in every season. You can try to create hand-made XNB mods for these too if you feel like it, but otherwise I suggest to skip this mod, as I think the default totems do not look that bad in the Victorian setting to worth the trouble.
- :green_heart: [SMAPI Seasonal Victoraian Buildings and Flowers](https://www.nexusmods.com/stardewvalley/mods/2050): A very nice recolor, that does well with the *Seasonal Victoraian Buildings and Flowers*. Use this Content Patcher version instead of any old one you find. After you start the game once and the config files are generated, you can edit the options for recolor, as written in the mod description.
  - This mod already contains :green_heart: [Ali's Flower Grass](https://www.nexusmods.com/stardewvalley/mods/2051): If you'd like a vivid Stardew Valley, this is the mod for you. Goes along perfectly with the Victorian style - you just have to set "UseEemieGrass": "false" (othervise it uses another grass mode) and "AliGrass": "Eemie" (or anything you like) in the config file.
- :green_heart: [Vintage Interface (Content Patcher)](https://www.nexusmods.com/stardewvalley/mods/1244): A very nice interface mod, which fits well with the victorian setting. It has one major drawback: it comes with **an own digspot mod, which cannot be disabled**, so if you install this, you will not be able to choose your own one. Also, some mod menus like *Mod Update Menu* will not have the updated style.
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
- :green_heart: [Climates of Ferngill](https://www.nexusmods.com/stardewvalley/mods/604): A nice mod that gives extra weather options to the game. What I have mainly noticed from it is that is often gets annoyingly foggy, but this mod is mainly for those who like to challenge them, even with the bad weather conditions: it can also be configured that the biggest storms constantly drain your stamina!

## 3. User Interface
- :heart: [Ui Info Suite](https://www.nexusmods.com/stardewvalley/mods/1150): Hands down one of the most useful mods in Stardew Valley. It adds indicators for various things: current luck, Queen of Sauce, bithdays, harvestable animal products, placable item ranges, NPC locations and other... None of these make the game too easy or ruin the fun, theye are selected very carefully and really make playing more comfortable.
Notice that be installing *Ui Info Suite* the following mods became redundant (and can cause error):
  - :yellow_heart: [CJB Show Item Sell Price](https://www.nexusmods.com/stardewvalley/mods/5): Shows sell price on items.
  - :yellow_heart: [NPC Map Locations](https://www.nexusmods.com/stardewvalley/mods/239): Shows NPC map locations (installing over *UI Info Suite* will display everything twice, and looks very bad).
  - :yellow_heart: [Range Display](https://www.nexusmods.com/stardewvalley/mods/1179): Range display for sprinklers, scarecrows, bee houses, and junimo huts.
  - :yellow_heart: [Simple Crop Label](https://www.nexusmods.com/stardewvalley/mods/314): Display the type of crop on mouse over - useful to see it when its still in seed state.
  - :yellow_heart: [Loved Labels](https://www.nexusmods.com/stardewvalley/mods/279): Display if the animal has been petted that day.
  - :yellow_heart: [Better Ranching](https://www.nexusmods.com/stardewvalley/mods/859): Shows harvestable animal product and love needed warnings on animals.
  - :yellow_heart: [Experience Bars](https://www.nexusmods.com/stardewvalley/mods/509): It is not the same to *UI Info suite*, as this shows the experiance bars constantly on the screen - but as the design isn't good and the bars are quite annoying, I don't recommend it.
  - :yellow_heart: [Lookup Anything](https://www.nexusmods.com/stardewvalley/mods/541): If you like it, go for it, but I think it's kind of an overkill. It is kind of an ingame Wikipedia, but the informations shown in other mods are enough for this, no need to install this one too.

___

<dl><dt>Choose one enemy healthbar mod:</dt></dl>

- :heart: [Enemies Health Bars](https://www.nexusmods.com/stardewvalley/mods/3627): Over the head, bigger, has numeric value (but configurable to hide). It also contains a fun feature: if you haven't killed enough monsters from the same type and/or your combat skill is not high enough, you only see a grey bar at their head. You only get more detailer health information when you have more experience, which is very immersive and fun. (This feature can also be disabled.)
- :green_heart: [HP Bar](https://www.nexusmods.com/stardewvalley/mods/1736): Under the creatures, smaller, does not have numeric value (but configurable to show).

___
- :heart: [Gift Taste Helper](https://www.nexusmods.com/stardewvalley/mods/229): A helpful mod thet shows the loved gift for each person in the calendar and in the Villagers menu (not inluding universally  loved gifts). If you feel like it's a cheat, you can modify the game's configuration to only show gifts that your character already knows if the person loves it, so you will have the opportunity to figure them out yourself.
- :heart: [Better Artisan Good Icons](https://www.nexusmods.com/stardewvalley/mods/2080): Really immersive addition to the game. With this, you can immediately see what kind of artistan goods you have in your inventory.
- :heart: [Fruit Trees with Signs](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-116#post-3347131) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/99 "Fruit Trees with Signs") page): Not exactly an UI mod but gives a little sign to your fruit trees that show which type of fruit they produce. Most useful in sapling phase, as trees almost all loke the same that time.
- :heart: ~~[Chest Label System](https://www.nexusmods.com/stardewvalley/mods/242)~~: A very good mod, but currently it's broken. If you want to replace it, I suggest using *[Chests Anywhere](https://www.nexusmods.com/stardewvalley/mods/518)*. However that mod know *way more* than we need, so if you want to use it only for chest labeling, I suggest you use the following settings in the config file: Range: None, EnableShippingBin: False and DisableInLocations: ["UndergroundMine"]


## 4. Character creation

<dl><dt>Choose one hair mod:</dt></dl>

- :heart: [Cute long hairstyles](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-4#post-3267152) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/910 "Cute long hairstyles") page): Adds 3 new hairstyles to the game, with 2 different variations.
- :heart: [Hairstyles recolored and a new Hairstyle Update](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-12#post-3278565) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/1103 "Hairstyles recolored and a new Hairstyle Update") page): My personal favorite, adds 21 new hairstyles to the game, plus their recolored versions (about 50 new hairs in total).
- :green_heart: [Improved and New Hairstyles](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-6#post-3273781) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/132 "Improved and New Hairstyles") page): Adds 12 new hairstyles to the game.
- :green_heart: [CRABBIT's new hair](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-12#post-3278197) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/1368 "CRABBIT's new hair") page): Adds a few new hairstyles to the game.
- :green_heart: [Dangan Ronpa Trigger Happy Havoc Female Hair and Shirts](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-64#post-3305998) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/163 "Dangan Ronpa Trigger Happy Havoc Female Hair and Shirts") page): Adds a bunch of new hairstyles and shirts to the game.
- :green_heart: [Karinas long hair](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-64#post-3305998) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/512 "Karinas long hair") page): Adds a 15 new hairstyles to the game.
- :green_heart: [More Hairstyles](https://www.dropbox.com/s/9976xv6s788uhs5/%5BCP%5D%20Pencilstab%27s%20Hair.zip?dl=0) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/91 "More Hairstyles") page): Adds a 16 new hairstyles to the game.

___

- :heart: [Get Glam](https://www.nexusmods.com/stardewvalley/mods/5044 "Get Glam"): A very important mod that adds a dresser to your farmhouse, where you can change your appearance (same as at the wizard, but free and always available). You didn't download those hair and clothes mod to only choose one and use it during the whole playthrough, did you?
  - :broken_heart: Note that [Kisekae](https://www.nexusmods.com/stardewvalley/mods/2348 "Kisekae") and [Get Dressed](https://www.nexusmods.com/stardewvalley/mods/331) are both broken.
- :heart: [Happy Birthday](https://www.nexusmods.com/stardewvalley/mods/520): If every villager has a birhtday, why don't you? This mod solves the problem: it lets you pick a date when all characters give you gift and compliments based on their heart level. A must-have immersive addition to the base game!
- :yellow_heart: [Kawaii Hats](https://community.playstarbound.com/threads/migrating-xnb-mods-to-content-patcher-packs.141577/page-54#post-3302982) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/64 "Kawaii Hats") page): Replaces the existing hats in the game with new ones, which can be cute, but they are mostly unimmersive and cringe. And it's not an extension: if you install it, you won't be able to access the game's basic hats.

## 5. Pets
- :heart: [Pet Interaction](https://www.nexusmods.com/stardewvalley/mods/4232): This mod gives you the ability to make your pet follow your through town (right click the pet for it) and play fetch with you. Who wouldn't want that power?
- :heart: [Cat Gifts](https://www.nexusmods.com/stardewvalley/mods/2132): Despite the name of the mod only mentions cat, both kind of pets will bring gifts for you if you install it. The frequency and the type of the items they give you at the begining of the day depends on your friendship level with the animal, but don't expect anything game-breaking. It's more of something that brings a smile on your face than money in your pocket (if you sell it, you heartless machine!).
- :green_heart: [Shiba Inu - Shepherd - Husky - Pet Dog Mod (CP)](https://www.nexusmods.com/stardewvalley/mods/570): With this mod you can change the type of your dog: the default is Shiba Inu (which has a little bit too big head for my taste), but you can choose from the three breeds mentioned in the title by editing the config.json file.
- :heart: [Pet Water Bowl](https://www.nexusmods.com/stardewvalley/mods/2009): Your pet's bowl will fill with water when it's raining or snowing. A nice little immersive touch to the game.
- :heart: [Improved Pet Area (Content Patcher Edition)](https://www.nexusmods.com/stardewvalley/mods/2026): This mod changes the look of the pet area next to your house to a more welcoming one. Your pet will have a separate food bowl and a blanket to lay on - it's really just a nice visual update.
- :heart: [Pet Choice Perks](https://community.playstarbound.com/threads/updating-mods-for-stardew-valley-1-4.156000/page-65#post-3360916) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/3313 "Pet Choice Perks") page): Based upon your choice of pet you can get unique advantages as a passive effect and on petting the animal: cats scare off crows and give fishing bonus, dogs make animals happier and give foraging bonus.

## 6. Villagers

- :heart: [Seasonal Villager Outfits](https://www.nexusmods.com/stardewvalley/mods/2449): This mod is awesome - it adds at least 4 separate outfits for every character, with other costumes such as wedding dresses, festival clothings or raincoats. This is unique and tailor-made (heh) for every character to match their personality, making the game more colorful and immersive. But the awesomeness does not stop here, because this mod also includes new portraits for every one of the clothes. These pictures are made with the original art style, and are perfectly integrated into the Stardew Valley feeling. However, it makes you unable to install any other character portrait mod, so if you want anime portraits or anything else, do not use this one.
- :green_heart: [Babies Take After Spouse Plus New Toddler Hair and Clothes](https://www.nexusmods.com/stardewvalley/mods/552): Your babies will look like your spouse, which is half-cute and nice and half-creepy as f. Decine which half you find stronger.

## 7. Gameplay

<dl><dt>Convinience mods:</dt></dl>

- :heart: [Yet Another Harvest With Scythe Mod](https://www.nexusmods.com/stardewvalley/mods/2731): This mods lets you harvest any plant using you scythe, which makes your farming much faster. I never had fun while I harvested bigger fields, with hundreds of cauliflower or pumpkin ripened at the same time, so I don't feel this mod unimmersive or cheaty.
  - :broken_heart: Note that [Harvest With Scythe](https://www.nexusmods.com/stardewvalley/mods/236) and [Scythe Harvesting v2.0](https://www.nexusmods.com/stardewvalley/mods/1106) are both broken.
- :heart: [Automate](https://www.nexusmods.com/stardewvalley/mods/1063): Automating every process on the farm makes your life so easy that it can even considered a cheat, but I just like the fact that I don't have to stand next to my furnace to make that 10 copper bar so much i don't even care about that. The main idea behind  this mod is that machines can take out ingredients from the chests around them and place ready products in them, but it has a _lot_ of usages, so I recommend checking out it's page before installing. Also, be careful, because it is not fun if your misplaced Charcoal Kilt converts all of your wood into coal... (actually, the next mod helpes with this problem).
- :green_heart: [Chests Anywhere](https://www.nexusmods.com/stardewvalley/mods/518): This mod is usually too much for what I call 'ideal game experience': accessing every chest from anywhere ruins the game, so if you want to use it that way, I change my rating to :broken_heart:. But if used well, this mod has a lot to offer: I already talked about a good use at the *Chest Label System* mod, which is broken, but van be replaced by this. It is also useful with *Automate*, as it has options to exclude a chest from autmating it's content by machines.
- :heart: [Convenient Chests](https://www.nexusmods.com/stardewvalley/mods/2196): Perfect mod, which offers two must have features: quick store items in a nearby chest where it is already present with Q and using items from nearby chests for crafting (without the need to directly put it in your inventory). These features get rid of 99% of frustrating item searching and storage management related flipping out.
- :heart: [Bigger Backpack](https://www.nexusmods.com/stardewvalley/mods/1845): Adds a forth row in you backpack which can be bought at Pierre's the same way as the other two.
- :green_heart: [Expanded Fridge](https://community.playstarbound.com/threads/updating-mods-for-stardew-valley-1-4.156000/page-52#post-3357251) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/1191 "Expanded Fridge") page): Adds cool purchusable features to the fridge (be sure to access it from the right side). These include multiple "chest pages" and a wrap-fridge you can access from anywhere. These sound a bit cheaty too, but you have to pay a decent price for them, and you can always choose to not buy them.
- :heart: [No Fence Decay](https://www.nexusmods.com/stardewvalley/mods/1180): Fences do not get broken, which I think was a very annoying thing in the base game.
- :green_heart: [Clean Cellar](https://www.nexusmods.com/stardewvalley/mods/2975): It gives a bit of an unbalanced advantage, as cellars will have more free space, but I mainly like this mod because the original, unclearable mess was annoying for me. But the vanilla one also has it's atmosphere, so decide if yo want to install this mod or not.
- :heart: [Horse Whistle](https://www.nexusmods.com/stardewvalley/mods/1131): Press the V button, and your horse will teleport to you, giving you the ability to make your way faster through the town. Must have mod.
- :heart: [AutoGate](https://community.playstarbound.com/threads/updating-mods-for-stardew-valley-1-3-closed.142524/page-55#post-3324704) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/820 "AutoGate") page): Adds cool purchusable features to the fridge (be sure to access it from the right side). This mod opens and closes gates on the fences where you get near them. A huge time/annoyance saver for every farmer!
- :heart: [Artifact System Fixed](https://community.playstarbound.com/threads/updating-mods-for-stardew-valley-1-4.156000/page-54#post-3357484) (For pictures check the old [Nexus](https://www.nexusmods.com/stardewvalley/mods/2761 "Artifact System Fixed") page): If you look at the mods description you can see numerous reasons why the artifact system needs a fix. For now, let it be enough that a random guy thought that it is not fair and some artifacts are ridiculously hard to get, and I agree with him, so I recommend you to install this.
- :yellow_heart: [Increased Artifact Spots](https://www.nexusmods.com/stardewvalley/mods/3340): Even with *Artifact System Fixed* it is really hard to restore the museums full collection, and it depends mostly on luck. This is why I like to 'alter' this luck a  bit, and have more artifact spots. But be careful! This mode gives *waay* too much artifact spots by default, so i suggest you to immediately edit the *config.json* for a more moderate setting (like 15 and false).
- :green_heart: [No Soil Decay Redux](https://www.nexusmods.com/stardewvalley/mods/1084): I really disliked when I dug up all my garden on the last day of a season just to see that on the next day I have to start it again if I want to plant any crops because they magically disappeared overnight. However this mod has a lot of issues: somethimes fertilizers still get removed (just the soil remains) and on the beggining of a new season sprinklers also only water the "supposedly remaining" tilled ground. It's also annoying that if you dig an artifact spot anywhere in town, that hole also remains there. So only install this mod, if you will hate tilling more than cleaning up digspots after yourself.

___

<dl><dt>Making the game more detailed:</dt></dl>

- :green_heart: [Minerva's Harder Community Center Bundles](https://www.nexusmods.com/stardewvalley/mods/3444): This mod is only recommended for those wo look for a real challenge. Minerva's Harder Community Center Bundles does exactly what it says - it makes restoring the Community Center *a lot* harder. Even the easy setting in this mod will test your best optimalization/management skills if you want to restore the building in a reasonable time. But at the same time doing so gives a real feeling of acomplishmenet: you can know you truly mastered living off the land.
- :green_heart: [Part of the Community](https://www.nexusmods.com/stardewvalley/mods/923): This mod introduces a lot new ways to improve friendship with villagers. For example, talking to someone will boost the relationship with those who witness it, or giving a gift also raises heart level with it's family members. There are some complains that this mod can make friendship too easy, but truth to be told, for me it was the least favourite part of the game when I had to run around the village and give everyone gifts to make them like me. This mod makes this process more reasonable, and if you find it too much of a cheat you can still modify the friendship increasement from the different actions in the config file.
- :heart: [Cooking Skill](https://www.nexusmods.com/stardewvalley/mods/522): Adds skill for cooking as the 6th available skill in the game, which is a welcomed addition. Cooked items will also have quality ratings from now, which mainly dpends on your skill.
- :heart: [Dragon's Advancing Sprinklers (Content Patcher)](https://www.nexusmods.com/stardewvalley/mods/4356): A real must have: you can now create higher level springlers with recipies using the lover levels. From now on the starting basic sprinklers won't go to waste!
  - :broken_heart: Note that [Advancing Sprinklers](https://www.nexusmods.com/stardewvalley/mods/2983) is broken.
- :heart: [Coffee Maker](https://www.nexusmods.com/stardewvalley/mods/4396): An elegant way to make coffee. It's really nothing else than a new item, but it's so well done it's a pleasure to have in your kitchen.
- :heart: [Better Panning](https://www.nexusmods.com/stardewvalley/mods/4161): Without any doubt, panning is the most useless Community Center reward. As the mod asks: "How many of you finish the fish tank and then place the copper pan into a chest to never be seen again?": so it adds better rewards (similar to a treasure chest) and improves placing for panning spots so you can actually reach them.
- :heart: [Better Quarry Redux](https://www.nexusmods.com/stardewvalley/mods/5170): Without any doubt, the quarry is the second most useless Community Center reward. But this mods improves the ore and geode chances in the quarry so it won't be like a quarter as effective as actually going to the mines. 
- :heart: [Winter Grass](https://www.nexusmods.com/stardewvalley/mods/1601): Makes grass grow in the winter too, so you don't have to rely on Marne for hay.
- :heart: [Working Fireplaces](https://www.nexusmods.com/stardewvalley/mods/3654): A new mechanic that makes the game a little harder but more interesting. In winter and on other rainy days you have to make a fire in your fireplace to keep yourself, your family and your pets warm. It even integrates with _Climates of Ferngill_ and makes use of the temperature data from that mod.
- :heart: [Cacti Hurt You](https://www.nexusmods.com/stardewvalley/mods/4019): A fun little mod that makes you lose a minimal heath when you bumb into a cactus.


## 8. Other mods

- :heart: [Skip Intro](https://www.nexusmods.com/stardewvalley/mods/533): Well, yeah, sorry ConcernedApe, but starting the game is just long.
- :heart: [Fast Animations](https://www.nexusmods.com/stardewvalley/mods/1089): If you were ever bored when you milked your 12 cows and goats or breaking up your 20 geodes at Clint, then this is just the mod for you.

# Finishing up

