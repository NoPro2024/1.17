# Migrating to 1.17

# Note

[Join my Discord for news regarding the development of this repository!](https://discord.gg/eXkMKCqtfQ)

If you would like to contribute, please make a PR.  
Some notes:
- Leave your name and GitHub link in the credits section, even for a tiny change
- Please try to use Modrinth/GitHub over Curseforge when applicable
- Please use a GitHub link instead of a Modrinth link for Author credit and avoid using Curseforge as best you can
- Make sure that the option to allow me to make changes to your PR is enabled

## Introduction

### The Situation

So, you've been playing on 1.8 for the past [5.5 years](https://howoldisminecraft189.today/) and are ready to see what 1.17 has to offer. Your first thought may be to download and install Forge and then add OptiFine as a mod, but this could not be further from the best choice. As Mojang have been been rolling out releases, they've also been decreasing performance with every version, and neither Forge nor OptiFine are really able to bring back even a speck of that performance that we see in 1.12 and below. However, another mod loader, Fabric, which is lightweight and easier to develop for, has created an amazing community in which many of its members focus on helping optimize the game to its greatest potential.

### Why no longer OptiFine?

OptiFine no longer provides the benefit that it once did on older versions of the game. As the years have gone by and Minecraft's code has changed, OptiFine has been continuing to completely overwrite major parts of Minecraft's code. Because OptiFine is closed source, it has become increasingly harder for modders to provide OptiFine compatibility. OptiFine also uses outdated formats for many of its features, including MCPatcher and its confusing and outdated settings menu. Many members in the Fabric community have taken it upon themselves to create better performance enhancing mods which surpass OptiFine, as well as provide alternatives to many of OptiFine's iconic features.

### Why no longer Forge?

TODO: Rewrite this entire thing but make it good

Forge has always been less than ideal for performance, because while it does try to fix vanilla issues relating to performance, it still has huge overhead for server-sided modding, which is not necessary for users wishing for a vanilla compatible experience. Fabric on the other hand is extremely lightweight and is practically identical to vanilla. It's also considered to be much easier to make mods for and has a great community, unlike Forge's community which is much more toxic. 

## Installing Fabric

TODO: Maybe images

0. Make sure you close Minecraft and the Minecraft launcher before installing Fabric, otherwise unexpected things can happen.
1. Download the [Fabric installer](https://fabricmc.net/use).
    - If you are on Windows, use the `.EXE` version of the installer on the right.
    - If you are on any other operating system or the `.EXE` version is not working for you, then use the `.JAR` version on the left.
2. Run the installer.
    - If you are using the `.EXE` version of the installer, simply double click the file. You may get a popup blocking you from running the installer and saying that "Windows protected your PC"; if so, then click on `More info` and then `Run anyway`.
    - If you are using the `.JAR` version, you will need to have Java installed on your device. If you have Java installed, then double click the downloaded file to run the installer. If you don't, then follow these steps:
        1. Go to the [Java downloads page](https://adoptopenjdk.net/?variant=openjdk8&jvmVariant=hotspot) and download the version of Java corresponding to your device.
        2. Run the Java installer by double clicking it.
        3. Do whatever the installer tells you to do.
        4. After installing Java, you should be able to run the Fabric installer by double clicking it. If you still can't for some reason, try running the program [Jarfix](https://johann.loefflmann.net/downloads/jarfix.exe).
3. Now that you have opened the installer, you will see two tabs at the top of the window: `Client` and `Server`. Make sure you are on the `Client` tab. Then, open the `Minecraft Version:` dropdown and select the version of Minecraft you want (most likely the latest version of Minecraft). The rest of the settings can be left with their defaults (unless you store your Minecraft version files in a different folder; if you want to use a different directory for this installation, that should be changed in the Minecraft launcher, not here). Click on `Install` when you are ready to install Fabric.
4. Once Fabric is finished installing, open your Minecraft launcher and click on the profiles button at the bottom left corner. Select the Fabric profile, it should be called something like `fabric-loader-1.17.x`. Then hit `PLAY` to start playing!
    - If you do not see the profile, try exiting and reopening the Minecraft launcher. If this also does not work, go to the `Installations` tab in the Minecraft launcher and make sure the `Modded` option is ticked on the rop right corner. If it still does not show up, create your own installation by clicking the `New installation` button, and selecting your desired fabric version in the `Version` dropdown. Then press `Create` and launch this installation.

## Installing Mods on Fabric

TODO: note about custom directories

0. Make sure you close Minecraft before installing mods, otherwise unexpected things can happen.
1. Open your Minecraft folder:
    - Windows: Click on the Start button at the bottom left corner of your screen. Then type in `%appdata%` and hit enter. Open the folder called `.minecraft`.
    - Mac: On the bar at the top of your screen in Finder, click `Go`, then click `Go to Folder` and type `~/Library/Application Support/Minecraft`, then hit enter.
    - Linux: Open `~/.minecraft`.
2. In your Minecraft folder, open the folder called `mods`.
    - If this folder does not exist, create it.
3. Place all of the mods you want to use into this folder (note that all mods you install must be for Fabric 1.17 or they will not work).

## Mods 

#### NOTE: If on Sodium 0.3, you will need to use [Indium](https://github.com/comp500/Indium) as well. Also, since Iris currently comes bundled with its own version of Sodium, it is not required to download Sodium standalone.

### Dependencies

These are essential mods that are pretty much required for most fabric mods as dependencies.

| Mod | Description | Author |
| --- | --- | --- |
| [Fabric API](https://modrinth.com/mod/fabric-api) | Required for most Fabric mods. | [Fabric Team](https://github.com/FabricMC) |
| [Mod Menu](https://modrinth.com/mod/modmenu) | Allows the user to see all installed mods, as well as access the config for most. | [Terraformers](https://github.com/TerraformersMC) |
| [Fabric Language Kotlin](https://www.curseforge.com/minecraft/mc-mods/fabric-language-kotlin) | Required for mods that run on Kotlin. | [Fabric Team](https://github.com/FabricMC) |

### Performance

These are mods that are needed for playing the latest versions of Minecraft at a reasonable FPS. These will also help decrease frame times, hopefully eliminating spikes or stuttering.

| Mod | Description | Author |
| --- | --- | --- |
| [Sodium](https://modrinth.com/mod/sodium) | **Currently comes bundled with Iris!** An all around performance mod, Sodium allows users to play the latest versions of Minecraft with high FPS, completely outperforming OptiFine, with some users seeing up to 8x their vanilla frames. Sodium also drastically improve visuals, providing a much better gameplay experience. | [Caffeine](https://github.com/CaffeineMC) |
| [Iris](https://irisshaders.github.io) | Iris is a shader loader that allows users to load up their favorite OptiFine shaderpacks, but with much higher FPS. Iris also provides performance enhancements when not using shaders, making it great for all users. | [coderbot](https://github.com/coderbot16) |
| [Hydrogen](https://modrinth.com/mod/hydrogen) | **No 1.17.1 Yet.** Hydrogen helps reduce the amount of memory the game takes up. While this is mostly meant for large modpacks, it does not hurt using it for a vanilla experience. | [Caffeine](https://github.com/CaffeineMC) |
| [Lithium](https://modrinth.com/mod/lithium) | Lithium helps improve the performance of many vanilla systems without changing their mechanics. | [Caffeine](https://github.com/CaffeineMC) |
| [Starlight](https://github.com/Spottedleaf/Starlight/releases) | Starlight completely rewrites the light engine to make loading chunks much quicker. | [SpottedLeaf](https://github.com/Spottedleaf) |
| [LazyDFU](https://modrinth.com/mod/lazydfu) | LazyDFU prevents the DataFixerUpper from doing anything until it is required, improving your Minecraft start times. | [astei](https://github.com/astei) |
| [Enhanced Block Entities](https://modrinth.com/mod/ebe) | **No 1.17.1 Yet.** Enhanced Block Entities improves block entities by making them used baked models instead, allowing for better performance, visuals (via better smoothlighting), and better resource pack customizability. | [FoundationGames](https://github.com/FoundationGames) |
| [FerriteCore](https://modrinth.com/mod/ferrite-core/versions) | FerriteCore further reduces memory usage and should be used in conjunction with Hydrogen. | [malte0811](https://github.com/malte0811) |
| [Entity Culling](https://www.curseforge.com/minecraft/mc-mods/entityculling) | EntityCulling culls entities you cannot see, increasing FPS. | [tr9zw](https://github.com/tr7zw)
| [Dynamic FPS](https://modrinth.com/mod/dynamic-fps) | Dynamic FPS reduces your FPS, and therefore reduces your system load, when tabbed out of the game. | [juliand665](https://github.com/juliand665) |

### Recommended

These are mods that I recommend you to use at all times. While they may not boost performance, they are mostly quality of life mods meant to better your experience.

| Mod | Description | Author |
| --- | --- | --- |
| [Item Model Fix](https://www.curseforge.com/minecraft/mc-mods/item-model-fix) | Item Model Fix fixes the gaps you see on items when holding them. This makes for a much more pleasant experience for most texturepacks. | [Pepper_Bell](https://github.com/PepperCode1) |
| [Borderless Mining](https://www.curseforge.com/minecraft/mc-mods/borderless-mining) | **No 1.17.1 Yet.** Borderless Fullscreen for Minecraft. | [comp500](https://github.com/comp500) |
| [Not Enough Crashes](https://modrinth.com/mod/notenoughcrashes) | Not Enough Crashes takes you to the main screen instead of exiting the game when you crash. | [natanfudge](https://github.com/natanfudge) |
| [CleanView](https://www.curseforge.com/minecraft/mc-mods/cleanview-fabric) | CleanView prevents self particles from appearing on your screen. | [LianMI](https://github.com/zlainsama) |
| [Smooth Scrolling Everywhere](https://www.curseforge.com/minecraft/mc-mods/smooth-scrolling-everywhere-fabric) | **No 1.17.1 Yet.** Smooth Scrolling Everywhere makes the scrolling in all menus smoother. | [Shedaniel](https://github.com/shedaniel) |
| [No Potion Offset](https://www.curseforge.com/minecraft/mc-mods/no-potion-offset/) | **No 1.17.1 Yet.** No Potion Offset prevents your inventory from getting shifted over when you have an active potion effect. | [Shedaniel](https://github.com/shedaniel) |
| [Controlling](https://www.curseforge.com/minecraft/mc-mods/controlling-for-fabric) | Controlling completely revamps Minecraft's controls menu, making it much easier to navigate and change keys. | [Jaredllll08](https://github.com/jaredlll08) |

### Other Cool Mods

These are mods that are more dependant on personal preferance than importance.

| Mod | Description | Author |
| --- | --- | --- |
| [No View Bobbing Screen Shake](https://modrinth.com/mod/viewbobbingmod) | No View Bobbing Screen Shake removes the screen shaking when view bobbing is turned on, leaving only the swaying hand. | [InboundBark](https://github.com/InboundBark) |
| [Slight GUI Modifications](https://www.curseforge.com/minecraft/mc-mods/slight-gui-modifications) | Slight GUI Modifications adds animations to many GUI elements. | [Shedaniel](https://github.com/shedaniel) |
| [Colored Lights](https://modrinth.com/mod/colored-lights) | **Crashes with Iris/Sodium.** Colored Lights adds colored lighting to Minecraft with its colors completely customizable via resource pack. | [Gegy](https://github.com/Gegy) |
| [Blur](https://modrinth.com/mod/blur-fabric) | Blur creates a nice blur effect when in menus and is completely customizable. | [Motschen](https://github.com/Motschen) |
| [No Fade](https://modrinth.com/mod/no-fade) | **No 1.17.1 Yet.** No Fade removes the fading animation that Mojang added between their splash screens. | [UltimateBoomer](https://github.com/UltimateBoomer) |

### OptiFine Replacements

As OptiFine is no longer recommended, here are some replacements for many of it's features that have not already been listed above.

| Mod | Description | Author |
| --- | --- | --- |
| [Sodium Extra](https://modrinth.com/mod/sodium-extra) | **No 1.17.1 Yet.** Visual toggles. Adds most of OptiFine's and some custom ones. | [FlashyReese](https://github.com/FlashyReese) |
| [Ok Zoomer](https://modrinth.com/mod/ok-zoomer) | Zoom. More customizable than OptiFine's. | [boredomh1](https://modrinth.com/user/277qw1N1) |
| [Bobby](https://modrinth.com/mod/bobby) | Higher render distances. More customizable than OptiFine's. | [Johni0702](https://github.com/Johni0702)
| [LambDynamicLights](https://modrinth.com/mod/lambdynamiclights) | Dynamic lights. More customizable than OptiFine's. | [LambdAurora](https://modrinth.com/user/rRnTb0fG) |
| [LambdaBetterGrass](https://modrinth.com/mod/lambdabettergrass) | Better grass and better snow. More customizable than OptiFine's. | [LambdAurora](https://modrinth.com/user/rRnTb0fG) |
| [Cull Leaves](https://modrinth.com/mod/cull-leaves) | Smart leaves. | [Motschen](https://modrinth.com/user/6YsSV9eP) |
| [Fabrishot](https://modrinth.com/mod/fabrishot) | Higher resolution Screenshots. | [ramidzkh](https://modrinth.com/user/z0r5biKh) |
| [Soaring Clouds](https://www.curseforge.com/minecraft/mc-mods/soaring-clouds) | **No 1.17.1 Yet.** Custom cloud height. | [Draylar](https://github.com/Draylar) |
| [Clear Skies](https://www.curseforge.com/minecraft/mc-mods/clear-skies) | Removes fog color banding on skybox. | [grondag](https://github.com/grondag) |
| [Custom Splash Screen](https://modrinth.com/mod/custom-splash-screen) | **No 1.17.1 Yet.** Custom loading screen colors. Does not support OptiFine format. | [TeamMidnightDust](https://github.com/TeamMidnightDust) |
| [FabricSkyboxes](https://modrinth.com/mod/fabricskyboxes) | Custom sky. Does not support OptiFine format. | [AMereBagatelle](https://modrinth.com/user/ifLBWnLs) |
| [Connected Textures](https://github.com/PepperCode1/ConnectedTexturesMod-Fabric/releases) | CTM. Does not support OptiFine format. | [Pepper_Bell](https://github.com/PepperCode1) |
| [Chime](https://modrinth.com/mod/chime) | **No 1.17.1 Yet.** CIT. Does not support OptiFine format. | [Emi](https://modrinth.com/user/R6WsWKy9) |
| [Colormatic](https://www.curseforge.com/minecraft/mc-mods/colormatic) | **No 1.17.1 Yet.** Custom colors. Does not support OptiFine format. | [Thalia](https://github.com/kvverti) |
| [Transparent](https://www.curseforge.com/minecraft/mc-mods/transparent-fabric) | **No 1.17.1 Yet.** Transparent textures. Does not support OptiFine format. | [Trikzon](https://github.com/Trikzon) |
| [Varied Mob Textures](https://www.curseforge.com/minecraft/mc-mods/varied-mob-textures) | **No 1.17.1 Yet.** Varied mob textures. Does not support OptiFine format. | [Digifox03](https://github.com/Digifox03/variedMobs) |

To convert from OptiFine format to a newer format, check out [MCPatcherPatcher](https://github.com/LambdAurora/MCPatcherPatcher) for compatible mods.

### Undecided

- kronhud (no 1.17 yet) https://www.curseforge.com/minecraft/mc-mods/kronhud
    - config isn't that good, doesn't get many updates, some features don't work last i checked  
- dashloader (has 1.17) https://modrinth.com/mod/dashloader/
    - compatibility nightmare

## Credits

- [NoPro2024](https://github.com/NoPro2024)
- [nacrt](https://github.com/nacrt)
- [Zordlan](https://github.com/Zordlan)
