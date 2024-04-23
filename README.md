#CREDITS FOR ASSETS USED
For the sound effects I utilized assets on opengameart.org and all the credits can be found within the actual code as well as here
Orbital Colossus.mp3 (background music) by Matthew Pablo

Laser3.wav, Laser11.wav, and Laser7.wav (shooting, explosion, and button sound effects) by dklon

8bit_bomb_explosion.wav (damage sound effect) by Luke.RUSTLTD

17.mp3 (healing sound effect) by Zoltan Milhalyi

Space Music.mp3 (background music) by Hitctrl

All of the visual elments such as the background, ship, text boxes, and meteors were all hand drawn by me

# Celestial-Voyage
Use "w" and "s" to move forward and back. Also use "a" and "d" to turn your ship left and right now use the space bar to help defend yourself against the onslaught of meteors that seek to ravage your ship.
#Game objects
Create a ship that the players controls on the game scene. This will be a simpleGE.sprite
		Set the image’s size and position
		Set a move speed for the ship by making a new attribute
		Make an attribute for the ship to have HP
	Define a process for moving the ship and turning it’s angle
		If the left key is pressed, add an amount to the ship’s current angle
		If the right key is pressed, subtract an amount from the ship’s current angle
		If the up  key is pressed, have the ship move forward in the direction it’s facing
		If the down key is pressed, have the ship move backwards


Create the bullets that ship will be able to fire. These will be called “Bullet” and will be a sprite
	Define the initializers to be self, scene, and parent
	Set the bullets color and size
	Set it so that when it hits the bounds it will hide
	
	Create a function for firing the bullets
		Have the bullet show itself
		Have the bullet be fire from the ship’s current position and angle
		Set the bullet’s movespeed

Create a new sprite for the meteors flying around the screen
		Set the image and size of the meteors
		Have it be able to reset by creating a new process
	Create a process for resetting the position of the meteors
		Create variable called “side” that is a random integer from 1 – 4
If a 1 is rolled
	Set the meteor to start at the top of the screen at a random width position
	Have it move down at a random angle between 180 and 360 degrees
	Have it move at a random speed
If a 2 is rolled
	Set the meteor to start at the right of the screen at a random height
	Have its move angle be set at a random angle between 90 and 270 degrees
	Have it move at a random speed
If a 3 is rolled
	Set the meteor to start at the bottom of the screen at a random width
	Have it move up via a random angle between 0 and 180 degrees
	Have it move at a random speed
If a 4 is rolled
	Set the meteor to start at the left of the screen at a random height
	Have it move to the right on a random angle between 90 and 270
	Have it move at a random speed
	Check for boundary detection
		When a meteor hits the border of the screen have it reset

Create a class for the game scene
		Set the background image
		Set an elapsed timer to record the time passed
		Set the base score to be “0”
		Create a variable for the number of meteors called “numMeteor”
		Create a variable for the max number of bullets
		Create a variable for current bullets
		Create a list for the sprites on screen

	Define processes for collision
		For the meteors on screen
			If a bullet collides with a meteor
				Reset the meteor
				Reset the bullet
				Add 1 to the score
			If the ship collides with a meteor
				Reset the meteor
				Subtract 1 from the ship’s hp
	If the ship’s hp reaches 0
		Stop the game and print out the player’s score and return to the instructions screen



Overview of the setting:
  In this universe, there lies infinite beauty that enriches the depths of one’s very soul. It is this enrichment that every being yearns for in their lifetime, and you being a drifter across the vast constellations are no different. So with a ship as your vessel of choice, you embark out into the vast astral sea and on your ventures you witness countless ethereal and mystical views that many have died trying to see in their lifetimes. However amongst the varied sights in space that spark awe, there are just as many entities that incite destruction and seek to wreak havoc on any voyager. The universe is not inherently good or bad, it is a beautiful amalgamation of conflictions and contradictions and unfortunately you have been dragged in on the cross fire. When traveling to another interstellar-landmark, you get caught in a time rift within a field of hurtling asteroids and they ravage your ship. You bear witness to your once home that sailed through the stars be torn asunder turning the once comforting sight of space into a horrifying realization of your demise. Just as everything goes dark and you feel oblivion itself grace your being, you awake to find yourself at the time at which you exactly entered the meteor field. Using your knowledge of how dangerous these celestial objects can be, you evade and even shoot them down as a means of carving out your escape route but no matter what you do, you can’t escape. Even after your ship is destroyed and you danced with death, you awake to the same scenario. You lost track of how long you’ve attempted this same orchestration, but one thing has become evidently clear, the once vast cosmos you’ve adored has now become an endless prison that not even death can penetrate. This is now your reality and you can either try your hardest to survive until you find a breakthrough or seek solace in knowing that in this world of unknown you can take comfort in knowing that you will at least return to a point of confined familiarity.
