SpaceCraft AutoPilot v3.6 by XrayIndia


### Terms of use ###

Do not redistribute the content of this pack without permission.

Credits are to be given whenever the content of this pack is featured in a save, dupe or media of any kind.


### Content ###

SpaceCraft Control v13.7 expression2
SpaceCraft AutoPilot v3.6 expression2
SpaceCraft Coordinates expression2
SpaceCraft Planetary Dock expression2
Resource System Container v1.1 expression2

Automatic spacecraft adv_dupe
Planetary consumer dock adv_dupe
Planetary generator dock adv_dupe
Consumer dock adv_dupe
Generator dock adv_dupe
Cargo hold adv_dupe


### Preliminary information ###

SCAP is still an experimental concept and it is very likely that you will encounter bugs while using it.
If this happens, refresh the expression(s) and try again.
Don't hesitate to report recurrent problems using the forum threads below.


### Setup instructions ###

SpaceCraft AutoPilot v3.6 uses SpaceCraft Control:

http://www.garrysmod.org/downloads/?a=view&id=125426

Be sure to read SCC's instructions first.


The easiest way to use SCAP is to spawn the adv_dupe of an functional ship that can be found in the adv_duplicator folder.
AFF model pack is needed for this:

http://www.garrysmod.org/downloads/?a=view&id=65313

Note: This ship is can not be piloted manually. To do so, please refer to the detailed instructions below.


To simulate a proper space environment, it is essential to remove air friction and prop gravity (and not player gravity).
You can set this using the console commands. If your console doesn't have these commands, install this addon:

http://www.garrysmod.org/downloads/?a=view&id=65191

and set the following:

phys_gravity_z 0
phys_airdensity 0

Note: SCAP will only activate hover thrusters during take off and landing.
Consequently, the ship will slowly fall down during any other flight sequence if gravity is on.
This may be a problem when using SCC with a high realism parameter.


Adv_dupe's controls:

+, - : Task selection
Enter : Set
. : Cancel

Further instructions are given by SCAP's menu.


The adv_duplicator folder also contains 4 types of docks: 2 space docks and 2 planetary docks.
Each of them is either generating resource or consuming resource.
Simply weld their base to your station or landing pad.


If you want to use SCAP on another prop, get the expression2s from the expression2 folder and follow these steps:

1. Spawn the SpaceCraft Control expression2 on a ship made of a single prop.
It is possible to spawn the expression on another prop and connect its "Scin" to an entity marker so the ship doesn't have to be the prop the E2 is welded to.
The same principle applies to the SpaceCraft AutoPilot expression2 (see below).
You will have to refresh the expressions after connecting Scin.
If the expressions are spawned directly on the ship to control, "Scin" doesn't have to be connected.

2. Spawn the SpaceCraft AutoPilot expression2 somewhere close to SCC.

3. Spawn the Coordinates expression2 somewhere close the the other expression2s.

4. Spawn a wire plug and weld it at the front of your ship.
The plug has to face towards the ship's forward() direction and the plug's up() has to be in the same direction as the ship's up().
If the plug is misplaced, docking might not work properly. Please refer to the adv_dupe for correct plug placement.

5. Spawn an entity marker close to the expressions and link it to the plug.

6. Spawn inputs for SCAP's menu: Next task, Previous Task, Set, Cancel. The best solution is to use a wire numpad.

7. Connect SCC's "Controls" wirelink input to SCAP. This will create a new wirelink output to SCAP.

8. Connect SCAP's "Coord" input to the Coordinates expression2.

9. Connect the Coordinates expression2's "Menu" input to SCAP's "Menu" output.

10. Connect SCAP's "Nextin", "Previn", "Enterin", "Cancelin" to your next task, previous task, set and cancel inputs.

11. Connect SCAP's "Plug" input to the entity marker linked to the plug.

12. Connect SCAP's "Plugwl" wirelink input to the plug. This will create a new wirelink output to the plug.

13. (optional) If you want the ship to be able to attack a target, place a weapon facing the ship's forward direction and connect the gun's trigger to SCAP's "Fire" output.


At this point, you should have an automatic spacecraft able to perform basics tasks.
However, as it isn't equipped with a cargo hold, it can not perform resource transport. It can also not be piloted manually yet.

To add a gargo hold, follow these steps:

1. Spawn the scap cargo hold adv_dupe from the adv_duplicator folder and weld it to the ship.

2. Connect SCAP's "Rs" wirelink input to RS Container v1 1, the expression2 attached to the cargo hold.

3. Connect Container's "In" input to the plug's "B" output.

4. Connect Container's "Out" input to the plug's "C" output.

5. Connect The plug's "B" input to Container's "Canin" output.

6. Connect The plug's "C" input to Container's "Canout" output.

7. (optional) if you want to display the resources in the cargo hold, connect a screen to Container's "Energypercent". The value is given in [%]

If you want to add manual controls to your automatic spacecraft, add the Input Manager and Camera Manager expressions from the SpaceCraft Control pack as decribed in the pack's instructions.
Then instead of connecting SCC's "Controls" wirelink input to Input Manager, connect SCAP's "Controls" wirelink input to Input Manager.
Manual controls are automaticly deactivated when the autopilot is on.

In case of problems, you can refer to the wire schematic included in the pack and to the adv_dupes.

The Planetary Dock expression2 has also been added for those who would like to make their own planetary dock.


### Forum threads ###

http://www.wiremod.com/forum/finished-contraptions/27445-spacecraft-autopilot-3-6-a.html#post245355

http://www.facepunch.com/threads/1126400?p=32374982#post32374982