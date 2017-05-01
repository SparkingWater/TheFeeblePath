# Advanced Game Programming 2016-17 - Assignment 2  
# Matthew Duddington

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Title.png "The Feeble Path”)

--------------------------------------------------------------------------------

## Team

**MA:**   
Pablo Larenas Henríquez
HungLi (Leo Cho)
Faris Omar

**MSc:**  
Nikita Veselov
Abdullah bin Abdullah
Matthew Duddington

(Additional assistance from Witek Gawlowski)

--------------------------------------------------------------------------------

## Aims  
### Group  

- Design a simple prototype slice of gameplay:  
  - Demonstrate the orientation of game mechanics for a multi-player environment.  
  - Include multiple animated characters and incorporation of AI.  

- Work with a new cross discipline team from the MA and MSc.  
  - Division of programming work into ‘owned’ components.  
  - Use of sprints and task lists to maintain a stable, remote-working, communication network.  
  - Scaling of ideas to fit the feasibility of implementation and stages of progress.  

### Individual 

- Become familiar with the handling of world states across server <-> client relationships.  
- Make use of more complex / sophisticated behaviours within Unreal Blueprints.  
- Utilise both inheritance and component approaches to assist with the sharing of intersecting tasks amongst the programming team.  

--------------------------------------------------------------------------------

## Design Overview  
### Deciding on the game format - ‘The Feeble Path’  

Initial designs proposed ranged from a Splinter Cell style cooperative sneak-em-up to racing fishes and even treasure hunting using Battleship mechanics. However, the team quickly voted to develop the ‘Obstacle Consequences’ format. Therein, each player would develop a small obstacle piece of a level, which would pass to their opponent who would attempt to complete it with their character, before supplementing it with their own additional obstacle and pass it back. This would cycle until a winner was determined.

This idea eventually grew towards a ‘labyrinth’ format and the idea of a stream of NPCs that would need to be guided through a maze of traps. After several iterations of this idea there appeared to be too many different elements combined together for the simple design we were aiming to achieve and so we stripped back the level design idea, as it was the most niche play style element, and instead focused on the interplay of NPCs and players. This also had the benefit of providing greater focus for the AI systems needed for Nikita and Abdullah’s connected module.

The Feeble Path design provided the security of requiring elements, that we were already familiar with achieving in Unreal (such as a dungeon based kit and interactive traps), with the challenge of both upgrading those elements to make use of a more complex context and interactive requirements, as well as incorporating concepts that were entirely new to us. This situation was true for both artists and programmers, who each had a set of specific requirements that needed to be met for their various modules.

*White board designs Feb 2017*  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/WB1a.jpg "White board designs Feb 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/WB1b.png "White board designs Feb 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Comms_Whiteboard2.jpg "White board designs Feb 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/WB2.png "White board designs Feb 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/WB4.png "White board designs Feb 2017”)  

### General Mechanics

- Cooperative play between 2 players.  
- Locate and guide ‘Feeble’ NPCs through a level safely.  
  - Feebles have a mood gradient that influences how they behave:  
    - Terrified: Run away, oblivious of traps, enemies and cliff edges.  
    - Frightened: Stand still, paralysed with fear; scream, attracting monsters.  
    - Calm: Follow the heros without causing trouble.  
    - Overconfident: Follow the heros, but insult monsters, attracting them.  
    - Bravado: Seek out risks, “attack” monsters, play with traps, walk along edge.  
- Solve interactive obstacles using differing, per-character, mechanics.  
  - Wizard is focused on ranged spells and manipulation of the environment.  
  - Knight is focused on melee contact, physical defence and weight.  

### Additional Information  

More detailed commentary on the design, as well as feedback on the process of the artists working with the programmers can be seen in the artists’ report:  
*http://www.pablolarenas.work/thefeeblepath*

--------------------------------------------------------------------------------

## Production Overview  

### Communication  

Because our working practices had worked very well in the original group project, we took several of the most effective approaches we had experienced and reapplied them. Early design meetings were highly inclusive and aimed to discuss and iterate on ideas at a rapid pace, we were able to conduct the majority of these meetings with most of the team within the same physical location. Production stages were split across in-studio working during the initial period, then moving to a mix of virtual and in-studio as different members of the team needed to work remotely.

Once again, we made extensive use of video conference calls / screen sharing, task lists via Trello initially and Google Spreadsheets latterly, and of course a significant amount of whiteboard discussion and diagrams.

*White board designs Feb - April 2017*  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/WB6.jpg "White board designs Feb - April 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/WB7.jpg "White board designs Feb - April 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/WB8.jpg "White board designs Feb - April 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/52a06c0f1ab4c7596dc5f2699a34cc88cb43684d/Reports/Images/WB9.JPG "White board designs Feb - April 2017”)  

*Trello and Google Spreadsheet communication lists Feb - April 2017*  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Comms_Trello2.png "Trello and Google Spreadsheet communication lists Feb - April 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Comms_Trello1.png "Trello and Google Spreadsheet communication lists Feb - April 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Comms_Google2.png "Trello and Google Spreadsheet communication lists Feb - April 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Comms_Google3.png "Trello and Google Spreadsheet communication lists Feb - April 2017”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Comms_Google4.png "Trello and Google Spreadsheet communication lists Feb - April 2017”)  

### My Role

Once again, because of my background in and familiarity with design, I performed a hybrid role on the team. However, because we had a more stable production art team, my input to the design side was mainly concentrated in the early stages, with just some continuing consultancy on technical art approaches, and Animation in particular, during the later stages.

Originally our team consists of only two programmers, Abdullah and myself; however, early on in the process we gained Nikita as an additional team member and, thus, had to readjust the responsibilities for the game production plan. Fortunately, this occurred before the core idea had been developed and so integration was straightforward.

This project was shared by three MSc modules, of which, because I am part-time, I am only undertaking one this year. Because of this my main advanced programming responsibility became the multiplayer considerations, with a view to guiding and refactoring the elements produced by Abdullah and Nikita so that they would be compatible with a server <-> client model. This proved to be a particularly challenging task, as many of the subtle interplays of how Unreal handles the resolution of ownership and variable replication were more unforgiving than any of the programming team anticipated. By the end of the project, however, the majority of the functionality was either multiplayer specific and mirrored precisely or, at least, multiplayer compatible with the main functionality resolved correctly on both sides. 

Whilst I was not on the AI module this year, and, thus, the two major parts of the character and enemy AI systems were handled by Nikita and Abdullah, I was involved with a significant amount of high level discussions of the AI design and implementation planning. Nikita requested multiple whiteboard sessions with me in order to work out approaches and alterations to certain sections of the AI system.

*White board AI discussion examples*  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/52a06c0f1ab4c7596dc5f2699a34cc88cb43684d/Reports/Images/AI_WB1.JPG "White board AI discussion examples”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/52a06c0f1ab4c7596dc5f2699a34cc88cb43684d/Reports/Images/AI_WB2.JPG "White board AI discussion examples”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/52a06c0f1ab4c7596dc5f2699a34cc88cb43684d/Reports/Images/AI_WB3.jpg "White board AI discussion examples”)  

My work with the design and art team was largely coordinated through Pablo, with occasional video calls to Leo to speak about Animation approach and improvements. During the first few weeks, I focused on the high level design of the game with the team, helping Pablo to guide the different ideas into potential game mechanic models. Due to the more ambitious requirements for the technical outcomes of this project, we were acutely aware of the need for design and programming to communicate effectively during the planning stage in order to produce a schematic that would be achievable by both halves of the team.

*Simplified demo level developed for the MVP*  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/52a06c0f1ab4c7596dc5f2699a34cc88cb43684d/Reports/Images/Demo_level1.png “Demo level birdseye”) 

Previously, I had worked as a project manager during the Global Game Jam event (which was described as a part of my earlier coursework). This role was suggested again for this team, however, while I was happy to fulfil that capacity, once Nikita had joined our team, I elected to hand the primary direction of the programming team to him, as he was particularly keen to practice this skill. Thus, while I maintained by role in tandem with Pablo, where more complex communication and coordination between art and programming teams was necessary, the main responsibility for programmer organisation was given to Nikita. However, in the final stages, this became slightly more blurry again, as Nikita gained an internship and had to excuse himself from some periods of the work process, and so I picked up some aspects of the programmer overseeing at that point.


--------------------------------------------------------------------------------

## Technical Overview

While the original intention was to make use of a blend of custom C++ and Blueprint within the project, once we began to explore the implementation of our idea, the programming team quickly realised that the requirements of what we needed to create was not only faster to create in Blueprint but also, from consulting the documentation, significantly more stable. As lead programmer, Nikita made the final decision that we would focus entirely on blueprint modules.

During initial discussions we considered using Photon engine as a backend to our multiplayer approach; it provides a library of functionality to handle several different types of multiplayer systems and has an implementation that links directly with Unreal. Ultimately, however, the decision was made to use the Unreal in-built systems, as we did not need complex and sophisticated multiplayer elements and so the Photon library may well have been overkill for our requirements. Also, we were keen to try and understand and practice with as much of the native Unreal functionality as possible before we replaced sections of it arbitrarily.

As mentioned above, my programming work on this project was predominantly focused on four areas:

- Interactive trap / obstacle implementation  
- Character skill implementation  
- Animation state machine linking  
- Multiplayer adaptation of blueprints  

Because I had worked with similar ‘traps’ in the previous Telement project, this time around I was challenged to adapt the single player and discreet approach taken last time, to an abstract / inherited and multi-player implementation.

When handling multiplayer, my investigations lead to understanding a series of rules that should be followed:

- The server version of the world, object and variable states should be considered cannon.  
- Where possible variables should be stored and updated only on the server, both for reliability and to prevent cheating.  
  - As few variables as possible should be subject to ‘replication’, in order to save on bandwidth.  
  - The exception to this is variables that are needed for decision making in aesthetic changes, such as changing a lever’s mesh’s position or updating each player’s UI.  
  - Where some behaviour should be triggered by the update of a variable, these values should be marked as ‘rep-notify’, and it’s corresponding linked function then used to trigger the behaviour.  
- Likewise, decision making or game mechanic centric functions should be run on the server, with return values that reflect the aspect of the outcome that the client side needs to be aware of.  
  - Functions such as overlap / hit will be triggered on all versions of the world, and thus, must be gated by checks for ‘authority’ when determining how and whether to process them.  
  - Conversely, any input signals will only be run on the client that they are owned by. Therefore, all inputs must trigger replicated functions to the server in order for it to be aware of these signals.  
- Any objects who’s reference is needed on both server and client sides must be marked for replication. e.g. Spawned objects and actors, and non-static elements.  

While developing my answers to these systems, I came across another important caveat that is specific to the Unreal platform. Two of the replication types for functions can only be called successfully inside blueprints that are attached to an object that has a “Net Owner”. This meant that I had to make many of my responses initially within the character owned objects rather than within the generic instigator, in order for them to fire correctly when called. Unfortunately this restriction is not immediately obvious, and I spend a great deal of time trying to debug the error-log absent, silent failure of these functions attempting to be called elsewhere but not being accepted.

*Extract from Unreal documentation explaining restriction on Server / Client specific replication functions*  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/b08db54463f9e6c2234e2394dc8495c9c0d51a57/Reports/Images/Multi5.png "Extract from Unreal documentation explaining restriction on Server / Client specific replication functions”)  

*Sequence showing the parallel out-of-sync world state when replication is not correctly handled*  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/b08db54463f9e6c2234e2394dc8495c9c0d51a57/Reports/Images/Multi1.png "Sequence showing the parallel out-of-sync world state when replication is not correctly handled”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/b08db54463f9e6c2234e2394dc8495c9c0d51a57/Reports/Images/Multi2.png "Sequence showing the parallel out-of-sync world state when replication is not correctly handled”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/b08db54463f9e6c2234e2394dc8495c9c0d51a57/Reports/Images/Multi3.png "Sequence showing the parallel out-of-sync world state when replication is not correctly handled”)  

*Early testing of the multiplayer with AI*
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/b08db54463f9e6c2234e2394dc8495c9c0d51a57/Reports/Images/Multi4.png "Early testing of the multiplayer with AI”)

Below I will provide some extracted examples of how this was manifest within my work on the project.

### Interactive objects

In order to cleanly call interactive objects, a parent class was setup with behaviour to be inherited. This abstracted the common functionality of checking for player proximity, handling interaction calls on the object and gating the updating of it’s rep-notify state variables.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Interactive_trigger.png “Interactive objects blueprint - Trigger element”)  

Similarly the calling of connected objects was also handled via an inherited function.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Interactive_connected.png “Interactive objects blueprint - Connected objects element”)  

The calling of the interaction is carried out within the player character blueprint, where it is replicated from the client, upwards to the server.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Player_character_interactive_handling.png “Player character blueprint - Handling of interactive objects element”)  

Within a specific interactive object without onward connected objects, such as a normal gate, this interaction call would simply run the aesthetic reaction on all clients (in this case the gate opening), as the state of the door has already been decided by the server at this point, due to the inherited functions.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Player_character_interactive_handling.png “Gate blueprint - Interaction outcome”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Interactive_objects2.png “Gate interactive object”)  

Similarly, interactive objects that have onward connections, such as a lever or button, both carry out their aesthetic reaction on all clients, and attempt to trigger the inherited connected objects function (seen earlier) which, because of its “Switch: Has Authority” node, will only continue to run on the server.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_lever.png “Switch, button and spikes interactive objects”) 
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/Interactive_objects1.png “Switch, button and spikes interactive objects”)  

Spikes and pillars have similar theories behind them. Unique qualities needing solutions for these were an interruptible animation that needed to cycle in sync for the spikes, and synchronised particle spawn and sound effects for the pillar.  

### Character skills

Similar to the interactive objects, the character skills were approached with inheritance. Initially these were prototyped by Abdullah and myself as stand alone skills, for more rapid testing.

However, early in the production process, Nikita decided to refactor these into a heavily abstracted parent class. The benefit of this ultimately would have been ‘black box’ expression of common skill behaviours and a single point of failure to investigate if a skill was malfunctioning. However, we later realised that the level of abstraction taken was too great overall, leading to some functionality that would only be used once in our demo (even if the projection was that it could expand in the future) being obfuscated by generic naming and multiple layers of nested functions. Unfortunately, this was especially problematic when it came to adapting for the multiplayer functionality, and the result was that I needed to refactor a lot of Abdullah, Nikita and my character skill blueprints into new versions that more greatly resembled the old approach.

From this I had the lesson reinforced for me that abstraction should be used where it naturally arises, rather than being sought for its own sake.

During the refactoring, I retained some high level ideas from Nikita’s approach, such as sharing a cool down inherited function and handling a queryable, skill level awareness of its current state.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Skill_parent_tick.png “Parent skill cool down tick function”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Skill_parent_use.png “Parent skill use functioning state recording”)  

As with the interactive objects, a ‘use’ call on a skill would run the connected behaviours in the relevant child class. In the case of the Fireball Skill, this spawned a fireball that was oriented towards the mouse cursor, raycast hit-point from the cameras perspective. This raycast had to be conducted on the specific client, as it was input specific, otherwise the function would appear to work correctly on the server, but on the client would always aim the fireball at [0,0,0]. 

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Fire_skill.png “Fire skill use call”) 

For the calling of skills, here the input handling needed to be processed on the client side and then passed as quickly as possible to the server to make decisions. Each character has an enum of their possible skills and a record of the active choice, when the player makes an input, this is filtered through the local record of the active ability and then the relevant server call is made. The server then handles the decision on whether the skill is actually ‘useable’ (shown earlier) and, if so, runs the relevant functions to handle this, some of which are then replicated back down to the client.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Wizard_skills.png “Wizard skills extract showing client to server input replication calls”)  

An element I had less experience of in Telement was linking the UI reactions to the world / player state variables. Because I was the most familiar with how the multiplayer system was functioning, I also handled this linking process. For the most part this was straightforward as the ‘active skill’ was always stored locally to the client.

However, getting the other player’s health to show alongside the owned player’s heath was more difficult, as this value was owned by another client’s object. I overcame this issue by having the player health updates, which needed to be handled on the server anyway, also update a shared blackboard space value that was precomputed into a percentage and thus could simply be absorbed by the UI each tick.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Widget_menu_example.png “UI menu icon updater”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_3rd_person_health.png “Health handler function for characters”)  

### Multiplayer loading / tracking

For the actual loading of players into the same world, we used the Unreal session handling nodes. I had some difficulty with getting this to work consistently across different network situations, so for our demo and MVP we relied on running both game instances on the same computer and connecting to local host.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_game_sessions.png “Unreal session handling setup”)  

The OnPostLogin function was used to keep a reference to each unique player and to enable to game to determine when both players were ready to spawn.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Game_mode_tracking.png “OnPostLogin event handling”)  

Spawning was handled by the GameMode object on the server, with the character actors instantiated first and then each player assigned to posses one of those actor pawns. This code went through several substantial iteration changes in order to discover the most reliable method for our needs.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Game_mode_spawn_v1.png “Spawn event version 1”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Game_mode_spawn_v3.png “Spawn event version 3”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Game_mode_spawn_v5.png “Spawn event version 5”)  

In many cases within the setup for certain multiplayer objects, it was not possible to know precisely how long it would take for both copies of the world to finish initialising. So in several cases a null check delay loop was inserted to ensure the necessary variable would be set before the game could start.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_example_non_null_loop.png “Null check delay loop”)  

### Animation State Machines 

As well as providing consultation advice to the artists as they were animating, I was responsible for setting up the animation state machines that would link their animations into the blueprint code. This involved defining the graph of connections between animation states, determining what the conditions should be to move into and out of those states and finally to set up notifications within the animations themselves.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Anim2_Wizard.png “Wizard animation state graph”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Anim2_Knight.png “Knight animation state graph”)  
![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Anim4_condition.png “Example condition change for an animation state swap”)  

Notifications enable frame specific behaviours to trigger, such as activating the wizard’s shield at the moment that his gesture suggests, without hard coding in a delay. This gives greater flexibility for the animation to be updated and for the designer to then appropriately update the notification’s frame reference themselves. When triggered, these notifications can play a sound or call a linked function.

![alt text](https://github.com/SparkingWater/TheFeeblePath/blob/7118a2d56c69fb1f9837854821b01adb0b221162/Reports/Images/BP_Anim1.png “Wizard animation event connections”) 


