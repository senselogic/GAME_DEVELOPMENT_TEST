# Unity Test

Minimalistic third person shooter game evaluating Unity gameplay and UI implementation skills.

## Instructions

*   Carefully read the game specification and the coding standard.

*   Create a **Unity Test** 3D project in **Unity 2017.3**.

*   Import the following assets (and nothing else) :

    *   https://assetstore.unity.com/packages/3d/environments/fantasy-landscape-103573
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/sci-fi-hero-handpainted-demo-106154
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-footman-handpainted-86576
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-grunt-handpainted-98187
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-lich-handpainted-91497
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-rock-golem-handpainted-94707
    *   https://assetstore.unity.com/packages/vfx/particles/cartoon-fx-free-109565
    *   https://assetstore.unity.com/packages/vfx/particles/war-fx-5669
    *   https://assetstore.unity.com/packages/tools/particles-effects/lowpoly-water-107563
    *   https://assetstore.unity.com/packages/essentials/beta-projects/textmesh-pro-84126
    *   https://assetstore.unity.com/packages/2d/fonts/bubble-font-free-version-24987
    *   https://assetstore.unity.com/packages/audio/music/six-styles-of-bgm-35941
    *   https://assetstore.unity.com/packages/audio/sound-fx/fantasy-sfx-32833
    *   https://assetstore.unity.com/packages/audio/sound-fx/weapons/futuristic-weapons-set-15644
    *   https://assetstore.unity.com/packages/audio/sound-fx/foley/fantasy-sfx-for-particle-distort-texture-effect-library-42146

*   Try to implement as much as you can of this game in maximum two days, preferably in the following order :

    *   The hero camera, animation, overlay, aiming, shooting, impact and death.
    *   The footman/grunt/golem/lich animation, navigation, aiming, attack, impact and death.
    *   The game-lost menu.
    *   The game-won menu.
    *   The game-paused menu.
    *   The game-title screen.
    *   The game-options screen.
    *   The enemy minimap.
    *   The text localization.

*   Do your best to apply the programming conventions explained in the coding standard document, especially the following rules :
    *   Write your types in **UPPER_CASE** : TANK_SHELL.
    *   Write your type members in **PascalCase** : Tank.ShootShell().
    *   Write your local variables and method parameters in **snake_case** : enemy_index. 
    *   Don't use acronyms, abbreviations or single-letter variables.
    *   Include the class name in the attribute and variable names.
    *   Align braces vertically.
    *   Use braces even for single statement blocks.

*   On the last evening, simply send us back a pack or archive of your work in progress using a file transfer web service like **wetransfer.com** or **transferbigfiles.com**.

## Description

The player controls a futuristic hero equipped with a fully automatic laser gun.

He must survive in a forestial area with many aggressive enemies.

They can be of four different types :

*   The footman, a small knight holding a spike.
*   The grunt, a fierce goblin holding an axe.
*   The golem, a rock creature with deadly fists.
*   The lich, a vicious witch shooting fireballs with her magical wand.

To win the game, the hero must eliminate all the enemies with his gun in only 3 minutes, without being killed.

## Game controls

The primary game control device is an X360-like gamepad controller.

*   Gameplay-mode :
    *   Left stick down/up : **Move Down/Up axis**.
    *   Left stick left/right : **Move Left/Right axis**.
    *   Right stick down/up : **Aim Down/Up axis**.
    *   Right stick left/right : **Aim Left/Right axis**.
    *   Right trigger : **Shoot button**.
    *   Start button : **Pause button**.
*   Menu-mode :
    *   Left stick down/up : **Move Down/Up axis**.
    *   Lower face button (A) : **Select button**.
    *   Right face button (B) : **Exit button**.

## Game entities

### The **game** :

*   Has a state.
*   Has a maximum duration.
*   Has an enemy list.
*   Has a hero.
*   Has a camera.
*   Has a camera overlay.

### The **game menu** :

*   Has a title.
*   Highlights the active option, which can be chosen with the Move Down/Up axis.
*   Selects the highlighted option with the **Select** button.
*   Can be left by pressing the **Exit** button.

### The **game-title screen menu** :

*   Plays the Chrono Storm background music in a loop.
*   Is made of :
    *   The **Unity Test** title.
    *   The **Start** option, to start a single-player game.
    *   The **Options** option, to change the game options.
    *   The **Exit** option, to exit the game.

### The **game-paused menu** :

*   Plays a game-paused sound once.
*   Appears by pressing the **Pause** button during a game.
*   Suspends the game.
*   Is made of :
    *   The **Resume** button, to resume the game.
    *   The **Restart** button, to restart the game.
    *   The **Quit** button, to go back to the title screen.
*   Can also be left by pressing the **Pause** button again.

### The **game-options screen menu** :

*   Plays a menu-change sound once.
*   Is made of :
    *   The **Language : French/English/German** pull down option.
    *   The **Fullscreen : on/off** pull down option.
    *   The **Back** button, to go back to the title screen.

### The **game-played screen** :

*   Plays the Car Race background music in a loop.
*   Shows the camera overlay (HUD).
*   Starts with a 5-seconds countdown.
*   Shows the game-lost menu if the hero is killed or if the available time is exhausted.
*   Shows the game-won menu if the hero has killed all the enemies before the available time is exhausted.

### The **game-over menu** :

*   Playes a custom music once.
*   Is centered.
*   Is made of :
    *   A big custom message.
    *   The **Score : ... points** message.
    *   The **Restart** button, to restart the game.
    *   The **Quit** button, to go back to the title screen.

### The **game-won menu** :

*   Is a game-over menu.
*   Plays a Jingle Win music once.
*   Shows a **Victory** message.

### The **game-lost menu** :

*   Is a game-over menu.
*   Plays a Jingle Win music once.
*   Shows a **Defeat** message.

### The **game-played overlay** :

*   Has a small "+" character in its center.
*   Has a temporary countdown timer starting at **5** seconds in its center, 
*   Has a score counter starting at **0** near the middle of the upper edge.
*   Has a time counter starting at **3:00** near the upper left corner.
*   Has a health bar (or counter) near the lower left corner.
*   Has an enemy minimap near the upper right corner.

### The **island** :

*   Is surrounded by a large sea plane at zero height.
*   Is the default landscape of the "Fantasy Landscape" asset 
    with its outermost borders lowered to remain under the sea surface.
*   Uses the meter as the distance unit.
*   Has **20** footmen, **10** grunts, **5** golems, **5** liches and the hero, spread over its land surface.

### The **character** :

*   Has a state
*   Can **stand** idle.
*   Can **turn** (without animation).
*   Can **walk** or **run**, more or less quickly, depending on its current ground speed.
*   Can **attack** with a hitting weapon, a shooting weapon or his fists, depending on its own abilities.
*   Can **get hit**.
*   Can **die**.
*   Has a health.
*   Has an attack delay.
*   Has a maximum forward walking speed.
*   Has a maximum forward running speed.
*   Has a maximum sideways walking speed.
*   Has a maximum turning speed.
*   Has a capsule collider.
*   Has a locomotion blend tree.

### The **hero** :

*   Is a character.
*   Is **2** meters tall.
*   Has an initial health of **100**.
*   Has an initial score of **0**, which is incremented by the initial health of the enemies he kills.
*   Can run at **6** meters per second.
*   Can shoot several laser rays per second.
*   Walks or runs when the Move axis is used.
*   Rotates to point his gun toward the hero camera target.
*   Shoots laser rays with its gun toward the hero camera target when the Shoot button is used.

### The **hero camera** :

*   Aims roughly 0.5m above the hero head.
*   Remains a few meters behind the hero character, 
    so that we can see his feet in the bottom of the screen when looking horizontally.
*   Can turn laterally and vertically up to **120** degrees per second.
*   Can look down at **-80** degrees.
*   Can look up at **+80** degrees.
*   Immediately gets closer to the hero if there is an obtacle between them.
*   Quickly gets back to its default distance otherwise.
*   Rotates when the Aim axis is used.

### The **laser ray** :

*   Is a thin stretched capsule.
*   Has a glowing effect.
*   Has a speed of **20** meters per second.
*   Has a direct hit damage of **25**.
*   Is shot from the gun tip toward what is pointed by the center of hero camera along its axis.

### The **hero spawn** :

*   Has a glowing particle effect.
*   Is where the hero starts the level.
*   Disappears after 5 seconds.

### The **enemy** :

*   Is a character.
*   Has an energy bar over its head when its close enough from the hero.
*   Can't hurt the other enemies.
*   Can turn at **180** degrees per second.
*   Runs toward the hero when it's in front of him and closer than **50** meters, or if the hero hits him.
*   Strafes sideways when the hero aims directly at him.
*   Randomly attacks the hero when it's close enough, at a maximum frequency of once per **4** seconds.

### The **enemy minimap** :

*   Has a circular shape.
*   Shows the enemies within a 50 meters radius around the player as dots.
*   Shows the farther enemies as small triangles pointing outside the minimap from its edge.

### The **footman** :

*   Is an enemy.
*   Has an initial health of **50**.
*   Is **1** meters tall.
*   Can run at **2** meters per second.
*   Can hit the hero with a damage of **25** using his spike.
*   Attacks the hero only when it's closer than **2** meters.

### The **grunt** :

*   Is an enemy.
*   Has an initial health of **100**.
*   Is **2** meters tall.
*   Can run at **4** meters per second.
*   Can hit the hero with a damage of **50** using his axe.
*   Attacks the hero only when it's closer than **2** meters.

### The **golem** :

*   Is an enemy.
*   Has an initial health of **200**.
*   Is **3** meters tall.
*   Can run at **2** meters per second.
*   Can hit the hero with a damage of **100** using his fists.
*   Attacks the hero only when it's closer than **2** meters.

### The **lich** :

*   Is an enemy.
*   Has an initial health of **75**.
*   Is **1.5** meters tall.
*   Can run at **2** meters per second.
*   Can hit the hero with a damage of **50** using his fireball.
*   Attacks the hero only when it's closer than **2** meters.
*   Aims a bit in front of the hero, based on its current speed and direction.

### The **lich fireball** :

*   Is a small ball.
*   Has a flame particle effect.
*   Has an initial speed of **10** meters per second.
*   Has a direct hit damage of **20**.

## Version

1.0

## Author

Eric Pelzer (ecstatic.coder@gmail.com).

## License

This document is licensed under the Creative Commons Attribution-NonCommercial 4.0 International.
