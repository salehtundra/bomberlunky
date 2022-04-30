# Bomberlunky
Author: Chris

## Abstract
This is a self project to create or at least work on Bomberman Roguelike game concepts I have been toying around with in my head. This README will contain all the ideas I came up with and will be a sort of design document to base decisions off of moving forward. Anyone interested in this idea can feel free on forking and implementing some features. This is very ambitious so most of this will probably not be implemented.

## Inspiration
Inspiration came from this video https://www.youtube.com/watch?v=1tCnVuPmHwI. Dedicated guy got me interested in the design of these games and what could be done with them had Hudson Soft really doubled down on modern tech and design philosophies before they were shut down.

## Concept
The idea is to mix Spelunky a roguelike with Bomberman. Taking subsections of levels and desiging them then providing random generation within the subsections and combining them randomly would produce a great way of doing level design where replayability is always unique to the player but the levels feel handcrafted. Every level will have one guaranteed power up treasure chest. Blocks will contain loot like diamonds and gold to buy at the shop in between levels. There is a focus on difficulty which the bomberman series is not known for. I want wide pools of enemies in each level grouping to choose from for levels to achieve difficulty, replayability, and variety.

I would like to implement a classic mode where you have either infinite lives or infinite coninutes, you keep the number of bombs, speed, and flame strength on death in this mode. This would kinda be like a mix of a Spelunky Seeded Run and a regular bomberman campaign. I would also like a roguelike mode where it is one life game over then do a new run.

I am focusing on singleplayer to avoid doing netcode for multiplayer even though that would be more popular if this were to be released publically. If it ever got to that point I would reconsider this stance as multiplayer is what bomberman is known for.

One adjustment I want to make is there is too much waiting and down time in bomberman games. I feel like that is why they haven't acheived the popularity they should. To combat this I would give the player the ability to detonate bombs prematurely at the start so speed and skill can determine speed of gameplay. Bombs would still go off after 3 seconds like normal.

## Worlds
List of all available worlds to visit, roughly each one will have 4 stages and hopefully a boss fight on the 4th stage. Difficulty tier denotes which world on the split route the player chose.
<table>
  <tr>
     <th>Name</th>
     <th>Description</th>
     <th>Difficulty Tier</th>
  </tr>
  <tr>
     <td>Jungle</td>
     <td>Forested area with river hazards and vine blocks, possible bridge or waterfalls to mix things up</td>
     <td>1</td>
  </tr>
  <tr>
     <td>Sea</td>
     <td>Underwater area, whirlpool and water current hazards, shipwrecks to mix things up</td>
     <td>2</td>
  </tr>
  <tr>
     <td>Volcano</td>
     <td>Firey area, lava to block paths, possible fire and heat hazards</td>
     <td>2</td>
  </tr>
  <tr>
     <td>Ice</td>
     <td>Frozen area, ice physics on movement if you did not find a special item in the previous Sea world. Frozen enemies that can thaw when blasted, snow covered hazards, blizzard hazard</td>
     <td>3</td>
  </tr>
  <tr>
     <td>Dark Caves</td>
     <td>Dark cavern area, hard to see if you did not find a special item in the previous Volcano world. Pits are a hazard here, as well as stalagmites. Maybe some open desert areas to mix things up</td>
     <td>3</td>
  </tr>
  <tr>
     <td>Ruins</td>
     <td>Ancient ruins area, could go with an Asian vibe, Egyptian vibe, or more of a Mayan/Aztec vibe depending on which is thematically more intresting. Focus on trap hazards and stone puzzles</td>
     <td>4</td>
  </tr>
  <tr>
     <td>Future</td>
     <td>Futuristic city area, featuring traveling tubes and teleporters. Think Futurama for themeing.</td>
     <td>5</td>
  </tr>
  <tr>
     <td>Past</td>
     <td>Wild West or Medieval theme? Not really sure on this one, wanted a dichotomy for future (Wild West theme is more interesting to me)</td>
     <td>5</td>
  </tr>
  <tr>
     <td>Sky</td>
     <td>Cloud area, focus on wind and weather hazards. Rain slows bombs, Hail creates ice physics, Drought speeds up bombs and intensifies length of flames, Windy moves bombs</td>
     <td>5</td>
  </tr>
  <tr>
     <td>Lab</td>
     <td>Scientific area featuring most of the tech and really mazelike design, focus on tech hazards and poisonous hazards</td>
     <td>6</td>
  </tr>
  <tr>
     <td>Horror</td>
     <td>Lovecraftian themed area, focus on nondirect hazards or conceptual hazards, psychological of nature</td>
     <td>6</td>
  </tr>
  <tr>
     <td>Space</td>
     <td>Outer space area, focus on comets and gravity hazards, alien like planets in the background, maybe solar radiation hazards</td>
     <td>6</td>
  </tr>
</table>

## Items/Power Ups
This is a list of all the powerups I would need to implement, most of these come directly from bomberman
<table>
  <tr>
     <th>Name</th>
     <th>Appearance</th>
     <th>Function</th>
     <th>Location of Aquiry</th>
  </tr>
  <tr>
     <td>Fire Up</td>
     <td>Flame</td>
     <td>Increase flame length</td>
     <td>Levels, Shop</td>
  </tr>
  <tr>
     <td>Bomb Up</td>
     <td>Cartoon bomb</td>
     <td>Increase limit of bombs placed concurrently</td>
     <td>Levels, Shop</td>
  </tr>
  <tr>
     <td>Speed Up</td>
     <td>Skate</td>
     <td>Increase movement speed</td>
     <td>Levels, Shop</td>
  </tr>
  <tr>
     <td>Speed Down</td>
     <td>Sandal</td>
     <td>Decrease movement speed</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Fire Down</td>
     <td>Small flame</td>
     <td>Reduce bomb flame</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Kick Bomb</td>
     <td>foot to bomb</td>
     <td>Allow pushing of bombs</td>
     <td>Level (rare), shop</td>
  </tr>
  <tr>
     <td>Sight Up</td>
     <td>Miner hat</td>
     <td>Increase light around field of vision, important for Dark Caves area</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Full Sight</td>
     <td>Tech glasses</td>
     <td>Full light around field of vision, negates Dark Caves</td>
     <td>Hidden treasure in Volcano region</td>
  </tr>
  <tr>
     <td>Spike Shoes</td>
     <td>Cleats</td>
     <td>Removes ice physics</td>
     <td>Hidden treasure in Ice region</td>
  </tr>
  <tr>
     <td>Extra Health</td>
     <td>Heart</td>
     <td>Adds one more hit point (3 is starting out amount?)</td>
     <td>Level (rare), Shop</td>
  </tr>
  <tr>
     <td>Wall Pass</td>
     <td>Wall pass lines</td>
     <td>Walk through walls except edges of screen</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Bomb Pass</td>
     <td>Bomb pass lines</td>
     <td>Walk through bombs you already placed</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Line bomb</td>
     <td>Line of bombs</td>
     <td>Create a line of all the bombs you have available in front of you</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Teleport</td>
     <td>Star Trek Beam</td>
     <td>Move 3 spaces in faced direction on button press (OP defensive measure)</td>
     <td>Hidden treasure in the Future region</td>
  </tr>
  <tr>
     <td>Jet</td>
     <td>Jetpack</td>
     <td>Move really fast until you hit a wall in a given direction on button press (OP escape measure)</td>
     <td>Hidden treasure in the Sky region</td>
  </tr>
  <tr>
     <td>Bait</td>
     <td>Meat</td>
     <td>Works well on horror enemies AI (defensive measure)</td>
     <td>Hidden treasure in the Past region</td>
  </tr>
  <tr>
     <td>Laser</td>
     <td>Ray gun</td>
     <td>Long range attack on button press that can't go through walls</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Flamethrower</td>
     <td>Flamethrower</td>
     <td>Long range blast that can destroy walls and anything in faced direction on buton press, makes you really slow for 10 seconds afterwards</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Remote Bomb</td>
     <td>Heartbomb</td>
     <td>Stops automatic explosion timer for bombs</td>
     <td>Shop</td>
  </tr>
  <tr>
     <td>Blast Shield</td>
     <td>Shield</td>
     <td>Creates a shield in front of you that only protects from incoming fire attack (OP defensive measure)</td>
     <td>Shop</td>
  </tr>
</table>

## Enemies
This is a list of the enemy designs I came up with and how they interact with the player. The AI patterns are based off a list I created separately.
<table>
  <tr>
     <th>Name</th>
     <th>Description</th>
     <th>AI Pattern</th>
     <th>Special Abilities</th>
     <th>Habitat/World Region</th>
  </tr>
  <tr>
     <td>Jungle Frog</td>
     <td>Hops around, green in color</td>
     <td>Dumb Determined</td>
     <td>None</td>
     <td>Jungle,Sea</td>
  </tr>
  <tr>
     <td>Bomb Frog</td>
     <td>Hops around, red in color</td>
     <td>Dumb Determined</td>
     <td>Becomes a bomb when killed, will explode after 3s</td>
     <td>Jungle, Volcano</td>
  </tr>
  <tr>
     <td>Flower</td>
     <td>Cute little flower, moves around at pure random</td>
     <td>Dumb Random Chaos</td>
     <td>None</td>
     <td>Jungle, Ruins (rare)</td>
  </tr>
  <tr>
     <td>Cave Bat</td>
     <td>Looks like a keese from Legend of Zelda</td>
     <td>Dumb Guided</td>
     <td>Pass over walls and bombs</td>
     <td>Jungle,Dark Caves</td>
  </tr>
  <tr>
     <td>Creeping Vine</td>
     <td>Leechlike green vine that worms its way along the ground</td>
     <td>Smart Guided</td>
     <td>None</td>
     <td>Jungle, Ruins (rare)</td>
  </tr>
  <tr>
     <td>Mole</td>
     <td>An average ground mole</td>
     <td>Dumb Determined</td>
     <td>Burrows underground to avoid attack</td>
     <td>Jungle,Dark Caves,Volcano (rare)</td>
  </tr>
  <tr>
     <td>Pigmy</td>
     <td>Little tribesman who chases after player most of the time, really fast</td>
     <td>Dumb Guided</td>
     <td>Fast</td>
     <td>Jungle, Ruins</td>
  </tr>
  <tr>
     <td>Tree Mimic</td>
     <td>Tree looking monster, quite deadly</td>
     <td>Smart Guided</td>
     <td>Slow, take multiple hits to defeat</td>
     <td>Jungle</td>
  </tr>
  <tr>
     <td>Snake</td>
     <td>Simple snake</td>
     <td>Dumb Random Chaos</td>
     <td>None</td>
     <td>Jungle,Dark Caves (rare), Ruins (rare)</td>
  </tr>
  <tr>
     <td>Submarine</td>
     <td>A mechanical machine with a small pair of cartoon eyes looking out a window</td>
     <td>???</td>
     <td>Can dive underground to avoid attack</td>
     <td>Sea</td>
  </tr>
  <tr>
     <td>Fish School</td>
     <td>A group of fish that can </td>
     <td>???</td>
     <td>Can separate to avoid blasts</td>
     <td>Sea</td>
  </tr>
  <tr>
     <td>Leviathan</td>
     <td>A large fish that takes up multiple spaces</td>
     <td>Dumb Guided</td>
     <td>Takes multiple hits</td>
     <td>Sea</td>
  </tr>
  <tr>
     <td>Crab</td>
     <td>Red crab</td>
     <td>???</td>
     <td>None</td>
     <td>Sea</td>
  </tr>
  <tr>
     <td>Shark</td>
     <td>A shark</td>
     <td>Smart Guided</td>
     <td>Can destroy blocks</td>
     <td>Sea</td>
  </tr>
  <tr>
     <td>Seaweed</td>
     <td>A bunch of green vines</td>
     <td>Dumb Guided</td>
     <td>Phases through walls, stunned on first hit, needs second while stunned to destroy</td>
     <td>Sea</td>
  </tr>
  <tr>
     <td>Charybdis</td>
     <td>Whirlpool with teeth</td>
     <td>???</td>
     <td>Can only be destroyed when sucking in things, pulls player or bomb within two spaces towards it</td>
     <td>Sea</td>
  </tr>
  <tr>
     <td>Flamekin</td>
     <td>Firey little guy</td>
     <td>???</td>
     <td>Attracted to bombs and flame</td>
     <td>Volcano</td>
  </tr>
  <tr>
     <td>Lava worm</td>
     <td>Firey worm that takes up multiple spaces</td>
     <td>Dumb Guided</td>
     <td>Takes multiple hits</td>
     <td>Volcano, Dark Caves (rare)</td>
  </tr>
  <tr>
     <td>Rock Mimic</td>
     <td>Wall looking thing</td>
     <td>???</td>
     <td>Pretends to be wall for suprise attack</td>
     <td>Volcano, Ruins, Horror</td>
  </tr>
  <tr>
     <td>Salamander</td>
     <td>Lizard thing</td>
     <td>???</td>
     <td>Burrows underground to avoid taking hits, loses a tail if hit from behind and survives once</td>
     <td>Volcano</td>
  </tr>
  <tr>
     <td>Bomb Eater</td>
     <td>???</td>
     <td>???</td>
     <td>Eats bombs, weak to fire damage only when eating a bomb, invulnerable otherwise</td>
     <td>Volcano</td>
  </tr>
  <tr>
     <td>Snow Queen</td>
     <td>Princess</td>
     <td>???</td>
     <td>Freezes bombs with long range attack removing detonation to explode unless triggered by other bomb</td>
     <td>Ice</td>
  </tr>
  <tr>
     <td>Mammoth</td>
     <td>Wolly Mammoth</td>
     <td>???</td>
     <td>Takes 4 hits to beat, destroys walls</td>
     <td>Ice</td>
  </tr>
  <tr>
     <td>Snowman</td>
     <td>Snowman</td>
     <td>???</td>
     <td>Freezes any bomb it comes in contact with, pass through bombs</td>
     <td>Ice</td>
  </tr>
  <tr>
     <td>Penguin</td>
     <td>Penguin</td>
     <td>???</td>
     <td>Can slide very fast if player is in line of sight</td>
     <td>Ice</td>
  </tr>
  <tr>
     <td>Wolves</td>
     <td>Wolves</td>
     <td>???</td>
     <td>Tend to attack together from multiple points</td>
     <td>Ice</td>
  </tr>
  <tr>
     <td>Polar Explorer</td>
     <td>Cartoon Eskimo</td>
     <td>???</td>
     <td>None</td>
     <td>Ice</td>
  </tr>
  <tr>
     <td>Skeleton</td>
     <td>Skeleton</td>
     <td>???</td>
     <td>Crumbles after hit, then needs to be blown up while crumbled to be destroyed or it will reform</td>
     <td>Dark Caves, Lab (rare), Horror (rare)</td>
  </tr>
  <tr>
     <td>Miner</td>
     <td>Cartoon Miner</td>
     <td>???</td>
     <td>Destroys walls</td>
     <td>Dark Caves</td>
  </tr>
  <tr>
     <td>Vampire</td>
     <td>Vampire</td>
     <td>???</td>
     <td>Can transform into Cave Bat to move over walls, hit by explosion in bat form transforms back to vampire, moves fast as bat (faster than normal cave bat)</td>
     <td>Dark Caves, Ruins (rare)</td>
  </tr>
  <tr>
     <td>Golem</td>
     <td>Rock monster</td>
     <td>???</td>
     <td>Only vulnerable to attacks from behind</td>
     <td>Dark Caves, Ruins</td>
  </tr>
  <tr>
     <td>Mudman</td>
     <td>Mudman</td>
     <td>???</td>
     <td>Dives underground to avoid attacks, takes 3 hits to destroy</td>
     <td>Dark Caves</td>
  </tr>
  <tr>
     <td>Ancient Construct</td>
     <td>Gear Golem</td>
     <td>???</td>
     <td>Takes 3 hits to beat, destroys walls</td>
     <td>Ruins</td>
  </tr>
  <tr>
     <td>Levitating Ship</td>
     <td>Alien UFO</td>
     <td>???</td>
     <td>Passes over walls and bombs</td>
     <td>Ruins</td>
  </tr>
  <tr>
     <td>Archaelogist</td>
     <td>Cartoon Archaelogist</td>
     <td>???</td>
     <td>None</td>
     <td>Ruins</td>
  </tr>
  <tr>
     <td>Mummy</td>
     <td>Mummy</td>
     <td>???</td>
     <td>Turns into a skeleton after bomb blast</td>
     <td>Ruins</td>
  </tr>
  <tr>
     <td>Wight</td>
     <td>Red Skeleton</td>
     <td>???</td>
     <td>Blocks frontal attacks with shield, crumbles after a hit and gets back up after a while, needs to be destroyed while crumbled</td>
     <td>Ruins, Horror</td>
  </tr>
  <tr>
     <td>Wheel</td>
     <td>Giant Wheel</td>
     <td>???</td>
     <td>Moves over walls and bombs, takes 2 hits to beat</td>
     <td>Ruins</td>
  </tr>
  <tr>
     <td>Hover Car</td>
     <td>Futurama Car</td>
     <td>Smart Guided?</td>
     <td>moves fast, moves over walls</td>
     <td>Future</td>
  </tr>
  <tr>
     <td>Robot</td>
     <td>Robot</td>
     <td>???</td>
     <td>moves fast, destroys walls, takes 2 hits to beat</td>
     <td>Future, Space</td>
  </tr>
  <tr>
     <td>Alien</td>
     <td>Little green dude with ray gun</td>
     <td>???</td>
     <td>can shoot a laser that triggers bomb explosion</td>
     <td>Future, Lab, Space</td>
  </tr>
  <tr>
     <td>UFO</td>
     <td>UFO with green dude inside</td>
     <td>???</td>
     <td>can shoot a laser that triggers bomb explosion, can pass over walls, can pass over bombs, becomes Alien on destruction</td>
     <td>Future, Lab, Space</td>
  </tr>
  <tr>
     <td>Environmental Man</td>
     <td>Flamethrower man</td>
     <td>???</td>
     <td>can shoot a flamethrower that triggers bomb explosion and wall destruction, moves slow afterwards for 10s</td>
     <td>Future</td>
  </tr>
  <tr>
     <td>Gunslinger</td>
     <td>Cartoon Cowboy</td>
     <td>???</td>
     <td>Can shoot a bullet that triggers a bomb explosion, can pass over bombs</td>
     <td>Past</td>
  </tr>
  <tr>
     <td>Bandito</td>
     <td>Cartoon Bandit</td>
     <td>???</td>
     <td>Can shoot a bullet that triggers bomb explosion, can pass over bombs</td>
     <td>Past</td>
  </tr>
  <tr>
     <td>Buffalo</td>
     <td>Buffalo</td>
     <td>???</td>
     <td>Moves very fast towards player if in range, takes 2 hits to beat</td>
     <td>Past</td>
  </tr>
  <tr>
     <td>Miner</td>
     <td>Cartoon miner</td>
     <td>???</td>
     <td>Destroys walls, can block frontal attacks with shield</td>
     <td>Past</td>
  </tr>
  <tr>
     <td>Crow</td>
     <td>Crow</td>
     <td>???</td>
     <td>Moves over walls, moves fast</td>
     <td>Past</td>
  </tr>
  <tr>
     <td>Cloud monster</td>
     <td>Lakitu</td>
     <td>???</td>
     <td>Can shoot random lightning at areas, can target bombs with lightning causing them to explode, moves over walls</td>
     <td>Sky</td>
  </tr>
  <tr>
     <td>Raindrop monster</td>
     <td>Raindrop</td>
     <td>???</td>
     <td>Moves fast, phases through walls</td>
     <td>Sky</td>
  </tr>
  <tr>
     <td>Plane</td>
     <td>Plane</td>
     <td>???</td>
     <td>Takes 2 hits to beat, moves over walls and bombs, moves fast</td>
     <td>Sky</td>
  </tr>
  <tr>
     <td>Eagle</td>
     <td>Eagle</td>
     <td>???</td>
     <td>moves over walls and bombs, moves fast</td>
     <td>Sky</td>
  </tr>
  <tr>
     <td>Pheonix</td>
     <td>Pheonix</td>
     <td>???</td>
     <td>Moves over walls, reappears after death after 30 seconds, immortal</td>
     <td>Sky</td>
  </tr>
  <tr>
     <td>Homonculus</td>
     <td>Mimic of player</td>
     <td>???</td>
     <td>Can lay bombs, can use shield to block flame, can pass through bombs and walls</td>
     <td>Lab</td>
  </tr>
  <tr>
     <td>Remote Detonator</td>
     <td>Scientist in hazard gear</td>
     <td>???</td>
     <td>Can detonate your bombs, performs a 5 second animation to do that when on screen, takes 2 bombs to beat</td>
     <td>Lab</td>
  </tr>
  <tr>
     <td>Tunneler</td>
     <td>Earthworm</td>
     <td>???</td>
     <td>Moves fast, can destroy walls, can dive underground to avoid damage</td>
     <td>Lab</td>
  </tr>
  <tr>
     <td>Marine</td>
     <td>Cartoon Marine</td>
     <td>???</td>
     <td>Can shoot 3 rockets at a clip to detonate bombs or destroy walls, can block damage with shield, takes 3 hits to beat.</td>
     <td>Lab</td>
  </tr>
  <tr>
     <td>Experiment</td>
     <td>Dead Space Hunter Necromorph</td>
     <td>???</td>
     <td>Immortal, moves over walls, bomb blasts stun for 10 seconds</td>
     <td>Lab</td>
  </tr>
  <tr>
     <td>Floating Eye</td>
     <td>eyeball monster</td>
     <td>???</td>
     <td>Passes over walls and bombs, can shoot laser to trigger bomb explosion, moves fast</td>
     <td>Horror</td>
  </tr>
  <tr>
     <td>Fish Dragon</td>
     <td>Fish Dragon</td>
     <td>???</td>
     <td>Can spawn little merpeople to crowd an area, can dive to avoid damage, takes 3 hits to beat</td>
     <td>Horror</td>
  </tr>
  <tr>
     <td>Squid monster</td>
     <td>Squid monster</td>
     <td>???</td>
     <td>Can invert your controls after 5 second animation, takes 3 hits to beat</td>
     <td>Horror</td>
  </tr>
  <tr>
     <td>Brainchild</td>
     <td>Bloodborne Winter Lanterns</td>
     <td>???</td>
     <td>Controls disabled when in line of sight for 2 seconds, can freeze bombs from detonating</td>
     <td>Horror</td>
  </tr>
  <tr>
     <td>Shapeshifter</td>
     <td>Black shapeshifter</td>
     <td>???</td>
     <td>Any enemy it passes through it will turn into and have the abilities of until it passes through another enemy</td>
     <td>Horror</td>
  </tr>
  <tr>
     <td>Ghostlike being</td>
     <td>Ghost</td>
     <td>???</td>
     <td>Immortal, can pass through walls and bombs, will detonate bombs it passes over</td>
     <td>Horror</td>
  </tr>
  <tr>
     <td>Astronaut</td>
     <td>Cartoon Astronaut</td>
     <td>???</td>
     <td>Can block attacks with shield, can shoot laser to destroy walls or bombs, takes 2 hits to beat</td>
     <td>Space</td>
  </tr>
  <tr>
     <td>Comet</td>
     <td>Comet</td>
     <td>???</td>
     <td>Moves very fast in one direction, destroys all walls it comes into contact with instantly, triggers bomb explosion if it comes into contact with a bomb</td>
     <td>Space</td>
  </tr>
  <tr>
     <td>Rocket</td>
     <td>Space Rocket</td>
     <td>???</td>
     <td>Moves very fast in one direction, passes over bombs and walls</td>
     <td>Space</td>
  </tr>
  <tr>
     <td>Probe</td>
     <td>Probe</td>
     <td>???</td>
     <td>Can invert your controls and can instantly trigger bombs from detonating within a certain radius after a 2 second animation</td>
     <td>Space</td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
</table>


## Bosses
This is a list of all the bosses I would need to implement, I can't even think about what these might be like
<table>
  <tr>
     <th>Name</th>
     <th>Description</th>
     <th>Special Abilities</th>
     <th>Habitat/World Region</th>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
  <tr>
     <td></td>
     <td></td>
     <td></td>
     <td></td>
  </tr>
</table>