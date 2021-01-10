COMP3770: FINAL PROJECT

GROUP 11: Dariq Ahmed, Michelle Hua, Hannah Stam, Liangliang Xu, Matt Zeidler

GROUP WORK BREAKDOWN

Hannah: Questions 1 & 2 - Player and 5 enemies

Michelle Hua: Question 3 & 4 - Collectables and Powerups

Liangliang: Questions 7 & 8 - Display (including scores display, pause/resume buttons, main menu button), Scenes

Matt: Questions 5 & 6 - Platforms, Level Generation

Dariq: Questions 5 & 6 - Platforms, Level Generation

Everyone: Question 10 - Extra powerup, Background music, Sound effects, Background terrain, Storyscene

SCRIPTS EACH INDIVIDUAL CODED:

Dariq Ahmed: makeSect1.cs, makeSect2.cs, LevelGenMasterL1.cs, LevelGenMasterL2.cs, LevelGenMasterL3.cs, makeDeathZone.cs, make1sectL1.cs, make2sectL1.cs, make1sectL2.cs, make2sectL2.cs, make1sectL3.cs, make2sectL3.cs, CeilingGenerator.cs, gameOver.cs

Michelle Hua: PlayerStats.cs, Enemy.cs, PickUp.cs, HealthPickUp.cs, Laser.cs, LaserTest.cs, Deathzone.cs, LevelComplete.cs, DisplayGameOver.cs, DisplayLevelComplete.cs, ToMenu.cs

Hannah Stam: PlayerController.cs, CameraFollow.cs, GolemContoller.cs, GolemDamageByPlayer.cs, GolemDamageToPlayer.cs, QlikContoller.cs, QlikDamageByPlayer.cs, QlikDamageToPlayer.cs, DeathlingContoller.cs, DeathlingDamageByPlayer.cs, DeathlingDamageToPlayer.cs, PaladinContoller.cs, PaladinDamageByPlayer.cs, PaladinDamageToPlayer.cs, RedpinContoller.cs, RedpinDamageByPlayer.cs, RedpinDamageToPlayer.cs, BulletController.cs

Liangliang Xu: DisplayBorad.cs, GameSelection.cs, inGameUI.cs, MainMenu.cs, SceneLoader.cs, StotryTelling.cs, SystemBar.cs

Matt Zeidler: makeSect1.cs, makeSect2.cs, LevelGenMasterL1.cs, LevelGenMasterL2.cs, LevelGenMasterL3.cs, makeHorizPlatform.cs, makeVerticPlatform.cs, make1sectL1.cs, make2sectL1.cs, make1sectL2.cs, make2sectL2.cs, make1sectL3.cs, make2sectL3.cs

BUGS/FUTURE WORK:

Laser: Used line renderer and was unable to get the player to shoot the laser through multiple enemies all at once (can only kill enemy if player clicks on the enemy). Everything else about the laser is working. Tried fixing this bug with 'RaycastAll' (LaserTest.cs) and ended up being able to select multiple players, but when applying 'mousePosition' to allow player to click in any direction, the same bug occured again - only allowing the player to kill the selected enemy.

Camera: Camera only starts following Player after the Player enters the first section generated beyond the start platform. Also, if the Player moves to the left, the script stops following. Normally this would be a good thing, but when the Player starts moving forward again, the camera jolts as it starts following again.

Section Gen: Near end of level, there's a chance enemies will spawn without the correct walkStart and walkEnd values. We looked through the code and did our best to debug it, but it seems that there's something with last section that's causing a small error there. The walkStart walkEnd variables pass correctly otherwise.

Spawning: Power ups and collectables occasionally spawn with an offset on the z axis. This prevents the Player from collecting them. This occurs only occasionally, and so far the spawning code in the level generation scripts usually works correctly. THis seems to only occur when prefabs are not plugged in properly, so we will test it out by making sure all levels have the righ prefabs plugged in.

POWER UP COLOURS:

Immunity = Blue, Shield = Yellow, Double Damage = Red, Teleport(Will change to grey when player collects 5) = Grey, Laser = White, Instant Kill = Green