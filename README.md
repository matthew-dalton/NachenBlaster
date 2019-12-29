# Nachenblaster

This project was developed in XCode, and is therefore only guaranteed to run in a MacOS environment (unless you're able to make the necessary adjustments).
The provided zip file 'Full_Nachenblaster.zip' contains all of the required files, but additional applications are required to run the program; they are described below.

1)  Install XQuartz: https://www.xquartz.org/
    (A)  Click the download link, open the downloaded .dmg file, double-click on XQuartz.pkg, and follow the installation instructions.
    (B)  Log out and log back in again.
    (C)  To verify the installation, open a Terminal window and run the command 'echo $DISPLAY'. That should produce one line of output that ends with 'org.macosforge.xquartz:0'.

2)  Install freeGLUT
    (A)  Install the homebrew package manager: https://brew.sh/
    (B)  Open a Terminal window and run the command 'brew install freeglut'.


After installing the above and decompressing 'Full_Nachenblaster.zip', you have two options to build and run the game:

1)  XCode: Open the XCode Project file provided in the zip file and press the play button in the top left corner.
2)  Terminal: Open terminal, and use the 'cd' command to travel to the 'Full_Nachenblaster' directory.
    (A)  Run the command 'cd DerivedData/NachenBlaster/Build/Products/Debug'
    (B)  Run the command './NachenBlaster'

'report.docx' contains descriptions of the class hierarchy used to implement the program, including important design decisions.

The remainder of this document is a description of the game, generously provided in the project spec written by Carey Nachenberg:

* In NachenBlaster, your job is to fly your spaceship through outer space, shooting down alien spacecraft and gathering the goodies that they drop. The higher the score you receive, the more respected you’ll be in Star Fleet.
* You fly the NachenBlaster – she’s not the newest spaceship on the planet, but she’s trusty as a 1997 Chevy Impala. The NachenBlaster comes equipped with a near-endless supply of cabbages that it can fire at the evil space aliens.
* There are three different types of aliens. One is the Smoregon ship. Smoregon are evil green broccoli-like aliens with weepy green ooze flowing from the eyelids on their feet. And of course, being aliens they love shooting Turnips at your NachenBlaster ship. Smoregon are especially useful to shoot down, because when you do, they often drop goodies that you can snag and use (like repair kits and flatulence torpedoes).
* Then there are the silver-colored enemy ships: Smallgon ships. Smallgons are evil aliens that closely resemble string cheese. They are much less wealthy than the Smoregons, so they never drop goodies when they’re shot down. But like Smoregons, they will often shoot Turnips at your ship if given the chance to do so.
* The final enemy is the Snagglegon flying saucer. Snagglegons are a nasty race of aliens who resemble three-day-old bananas stolen from B-Plate, covered in fuzzy black mold (don’t act innocent, we know you know what those look like). Snagglegons are extremely aggressive and have much newer ships than the Smallgons or Smoregons. They also happen to possess a magic life-saving kit which they sometimes drop when their ships are destroyed. Snagglegons also have deadlier weapons, and shoot Flatulence Torpedoes at your ship instead of the usually nasty turnips.
* At the start of each game, your ship is placed in outer space and must save humanity by destroying the aliens. You start with 3 total ships (your active ship and two spares should your craft be tragically destroyed). Once you’ve destroyed enough of the aliens on the current level, the level will be over. Assuming you succeed in destroying enough of the aliens, you’ll then proceed to the next level where even more alien ships will come at you. And of course, in each new level, the enemy ships become more difficult to destroy (having more health points, also known as hit points). On and on the game goes until all of your ships are destroyed and you die. If your ship gets destroyed before the end of a level (and you still have a spare ship), then you have to replay the entire level over from scratch. Such a depressing game.
* Your NachenBlaster ship can move up, down, left and right. Your ship can and will often collide with enemy ships; this won’t necessarily destroy your ship outright, but will do a significant amount of damage, so it should be avoided. On the upside, if your ship collides with an enemy ship, it will always destroy the shoddily-built enemy ship. Your ship can fire cabbages, and, if you’ve been lucky enough to snag some off of a Smorgon, it can also fire Flatulence Torpedoes – which do much more damage than your slimy cabbages.
* You control the direction of your ship with the arrow keys, or for lefties and others for whom the arrow key placement is awkward, WASD or the numeric keypad: up is w or 8, left is a or 4, down is s or 2, right is d or 6. Use the space key to fire cabbages, and the tab key to fire Flatulence Torpedoes, if your ship has any. To pause the game, press 'f'; when you do this, the next key you should press is 'r', which resumes the game. Pressing any other key while the game is paused causes it to advance one tick at a time, but without moving nor shooting capabilites. To quit the game at any time, press the ‘q’ key.
