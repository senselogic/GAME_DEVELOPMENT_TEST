![](https://github.com/senselogic/UNITE/blob/master/LOGO/unite.png)

# Unite

Unity game development test.

[![](https://img.youtube.com/vi/xqOMwkJBuXE/0.jpg)](https://www.youtube.com/watch?v=xqOMwkJBuXE)

## Instructions

*   Carefully read the game specification and the coding standard.
*   Install the lastest stable version of [**Unity**](https://unity3d.com/fr/get-unity/download).
*   Create a **Unite** 3D project.
*   Import the following assets (and nothing else) :
    *   https://assetstore.unity.com/packages/3d/environments/fantasy-landscape-103573
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/sci-fi-hero-handpainted-demo-106154
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-footman-handpainted-86576
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-grunt-handpainted-98187
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-lich-handpainted-91497
    *   https://assetstore.unity.com/packages/3d/characters/humanoids/mini-legion-rock-golem-handpainted-94707
    *   https://assetstore.unity.com/packages/vfx/particles/cartoon-fx-free-109565
    *   https://assetstore.unity.com/packages/tools/particles-effects/lowpoly-water-107563
    *   https://assetstore.unity.com/packages/essentials/beta-projects/textmesh-pro-84126
    *   https://assetstore.unity.com/packages/2d/fonts/bubble-font-free-version-24987
    *   https://assetstore.unity.com/packages/audio/music/six-styles-of-bgm-35941
    *   https://assetstore.unity.com/packages/audio/sound-fx/fantasy-sfx-32833
    *   https://assetstore.unity.com/packages/audio/sound-fx/horror-sfx-32834
    *   https://assetstore.unity.com/packages/audio/sound-fx/sci-fi-sfx-32830
    *   https://assetstore.unity.com/packages/audio/sound-fx/foley/fantasy-sfx-for-particle-distort-texture-effect-library-42146
*   Try to implement as much as you can of this game in maximum two days, preferably in the following order :
    *   The hero camera
    *   The hero aiming, shooting and death.
    *   The footman/grunt/golem/lich patrolling, chasing, attack and death.
    *   The level-played panel
    *   The level-loaded panel.
    *   The level-started panel.
    *   The level-paused panel.
    *   The mission-failed panel.
    *   The mission-complete panel.
    *   The game-loaded panel.
    *   The game-started panel.
    *   The game-options panel.
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

The player uses a gamepad to control a futuristic hero equipped with a fully automatic laser gun.

The hero must survive in a forestial area with many aggressive enemies.

They can be of four different types :
*   The footman, a small knight holding a spear.
*   The grunt, a fierce goblin holding an axe.
*   The golem, a rock creature with deadly fists.
*   The lich, an undead magician shooting fireballs with his staff.

To win the game, the hero must reach an elimination score of 1000 points in maximum 3 minutes, without being killed.

## Game entities

### The game

*   Has several panels.
*   Has a language.
*   Has an instance.
*   Has a state.

### The game input

*   Uses a mouse for the menus, and an X360 gamepad for the gameplay.
*   Provides :
    *   4 axes :
        *   Left stick down/up : **Move Down/Up axis**.
        *   Left stick left/right : **Move Left/Right axis**.
        *   Right stick down/up : **Aim Down/Up axis**.
        *   Right stick left/right : **Aim Left/Right axis**.
    *   2 buttons :
        *   Right trigger : **Shoot button**.
        *   Start button (or Escape key) : **Pause button**.

### The **game-loaded** panel

*   Has a game name title.
*   Has a loading progress bar.

### The game-started panel

*   Has a game name title.
*   Has a **Start** button, to start a single-player game.
*   Has an **Options** button, to change the game options.
*   Has an **Exit** button, to exit the game.
*   Plays the **Chrono Storm background music** in a loop.

### The level-paused panel

*   Has a **Resume** button, to resume the level.
*   Has a **Restart** button, to restart the level.
*   Has a **Quit** button, to go back to the game-started panel.
*   Appears by pressing the **Pause** button during a game.
*   Suspends the game.
*   Can be left by pressing the **Pause** button again.

### The game-options panel

*   Has a **Music** volume slider
*   Has a **Sound** Volume slider
*   Has a **Language (English/French)** pull down menu.
*   Has a **Back** button, to go back to the game-started panel.

### The **level-loaded** panel

*   Has a level name title.
*   Has a loading progress bar.

### The level-started panel

*   Has a **5-seconds countdown**.
*   Plays a beep sound on each second.

### The level-played panel

*   Has a **score counter** starting at **0** near the upper right corner.
*   Has a **remaining time counter** starting at **3:00** near the middle of the upper edge.
*   Has a **health bar** near the lower left corner.
*   Has a **circular minimap** near the lower right corner.

*   Plays the **Car Race background music** in a loop.

### The mission-complete menu

*   Has a **Mission complete** message.
*   Has a **Restart** button, to restart the level.
*   Has a **Quit** button, to go back to the game-started panel.
*   Plays a **Jingle Win music** once.
*   Appears when the score is superior or equal to 1000 or all enemies have been killed.

### The mission-failed panel:

*   Has a **Mission failed** message.
*   Has a **Restart** button, to restart the level.
*   Has a **Quit** button, to go back to the game-started panel.
*   Plays a **Jingle Lost music** once.
*   Appears when the hero is killed or there is no more remaining time.

### The level

*   Has a maximum duration.
*   Has a hero spawn.
*   Has a hero.
*   Has a hero camera.
*   Has an enemy spawn array.
*   Has an enemy array :
    *   **10** footmen.
    *   **10** golems.
    *   **10** grunts.
    *   **10** liches.
*   Has a state.
*   Has an instance.

*   Uses the default landscape of the **Fantasy Landscape** asset
    with its outermost borders lowered to remain under the sea surface.
*   Is surrounded by a large sea plane at zero height.
*   Uses the meter as the distance unit.

### The character

*   Can stand idle.
*   Can turn at **120** degrees per second (without animation).
*   Can walk.
*   Can attack.
*   Can die.
*   Has a health.
*   Has an attack delay.
*   Has a maximum forward walking speed.
*   Has a maximum forward running speed.
*   Has a maximum sideways walking speed.
*   Has a maximum turning speed.
*   Has a capsule collider.
*   Has a locomotion blend tree.
*   Has a state

### The hero

*   Is a character.
*   Is **2** meters tall.
*   Has an initial health of **100**.
*   Has an initial score of **0**, which is incremented by the initial health of the enemies he kills.
*   Can walk forward and backward at **4.5** meters per second.
*   Can walk sideways at **3** meters per second.
*   Can hit enemies using his laser gun ray.
*   Walks or runs when the Move axis is used.
*   Rotates to point his gun toward the hero camera target.
*   Has a laser gun.

### The hero camera

*   Aims above the hero head.
*   Remains a few meters behind the hero character,
    so that we can see his feet in the bottom of the screen when looking horizontally.
*   Can turn laterally and vertically at **120** degrees per second.
*   Can look down at **-5** degrees.
*   Can look up at **+10** degrees.
*   Immediately gets closer to the hero if there is an obtacle between them.
*   Quickly gets back to its default distance otherwise.
*   Rotates when the Aim axis is used.

### The hero laser gun muzzle

*   Can shoot a laser ray **5** times per second toward the hero camera target when the Shoot button is used.

### The hero laser gun ray

*   Is a thin stretched capsule.
*   Has a speed of **50** meters per second.
*   Has a direct damage of **10** on enemies once per shot.
*   Is shot from the gun tip toward what is pointed by the center of hero camera along its axis.

### The enemy

*   Is a character.
*   Can't hurt the other enemies.
*   Can turn at **120** degrees per second.
*   Can walk forward at **4.5** meters per second.
*   Chases the hero if :
    *   the hero is near and in front of him.
    *   the hero has hit him.
    *   a nearby enemy is chasing the hero.
    *   a nearby enemy has been killed.
*   Randomly attacks the hero when it's close enough, at a maximum frequency of once per **4** seconds.

### The enemy minimap

*   Has a circular shape.
*   Shows the active enemies within a 50 meters radius around the player.

### The footman

*   Is an enemy.
*   Has an initial health of **50**.
*   Can walk forward at **4.5** meters per second.
*   Can hit the hero with his spear.

### The footman spear tip

*   Has a direct damage of **100** on the hero once per attack.

### The grunt

*   Is an enemy.
*   Has an initial health of **100**.
*   Can walk forward at **4.5** meters per second.
*   Can hit the hero with his axe blade.

### The grunt axe blade

*   Has a direct damage of **100** on the hero once per attack.

### The golem

*   Is an enemy.
*   Has an initial health of **200**.
*   Can walk at **2** meters per second.
*   Can hit the hero using his fists.

### The golem fist

*   Has a direct damage of **100** on the hero once per attack.

### The lich

*   Is an enemy.
*   Has an initial health of **75**.
*   Can walk forward at **4.5** meters per second.
*   Can hit the hero using his staff fireball.

### The lich staff tip

*   Can shoot a fireball every 2 seconds.

### The lich fireball

*   Has a diameter of **0.5** meters.
*   Has a flame particle effect.
*   Has an initial speed of **10** meters per second.
*   Has a direct damage of **25** on the hero once per shot.

## Version

1.3

## Author

Eric Pelzer (ecstatic.coder@gmail.com).

## License

This project is licensed under the GNU Lesser General Public License version 3.

See the [LICENSE.md](LICENSE.md) file for details.
