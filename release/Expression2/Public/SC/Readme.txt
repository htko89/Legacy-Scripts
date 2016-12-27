SpaceCraft Control v13.7 by XrayIndia


### Terms of use ###

Do not redistribute the content of this pack without permission.

Credits are to be given whenever the content of this pack is featured in a save, dupe or media of any kind.


### Setup instructions ###

The easiest way to use SCC is to spawn the adv_dupe of an operational ship that can be found in the adv_duplicator folder.
Eternal Silence's ship pack is needed to spawn it:
http://www.garrysmod.org/downloads/?a=view&id=63344

You need to sit in the seat that spawns next to the ship to pilot it.


To simulate a proper space environment, it is essential to remove air friction and prop gravity (and not player gravity)
You can set this using the console commands. If your console doesn't have these commands, install this addon:

http://www.garrysmod.org/downloads/?a=view&id=65191

and set the following:

phys_gravity_z 0
phys_airdensity 0

SCC can also fly under atmospheric conditions (gravity + air).
Use hover thrusters (see below) if stabilisation thrusters aren't powerful enough to lift the ship.


SpaceCraft Control is designed to be used with a joystick using Night-Eagle's joystick module, which can be found here:

http://www.facepunch.com/threads/403669-gmcl_joystick-DirectInput-module-with-simplified-interface

Joystick bindings have to match the following configuration:

1: Pitch
2: Yaw
3: Roll
4: Throttle (forward)
5: Reverse
6: Translation mode activation (keep pressed)
7: Translation Stabilisation Deactivation (keep pressed)
8: Hover thrusters activation

Extra controls:

Space: Manual thrust control
WASD: Translation
Mouse1: External view (if you get the seat's 3rd person view, press control)
Mouse2: Cockpit mouse view (keep pressed, doesn't work well unless the seat is welded to the ship)


SCC can also be controlled using only the keyboard. To do so, simply disconnect the SpaceCraft Input Manager expression2's "Joy" wirelink input.
Nevertheless, this significantly reduces SCC's precision.

Space: Throttle (forward)
R: Reverse
WS: Pitch
AD: Roll
Shift: Translation mode activation (keep pressed)
Shift + R: Hover Thrusters activation
Alt: Translation Stabilisation Deactivation (keep pressed)
Mouse1: External view (if you get the seat's 3rd person view, press control)
Mouse2: Cockpit mouse view (keep pressed, doesn't work well unless the seat is welded to the ship)


Hover thrusters work exactly like stabilisation thrusters but are more powerful and only apply positive vertical force.
This means they can only be controlled when in translation mode. They don't automaticly maintain the ship's altitude.

To adjust realism (Thrusters' maximum force), open the SpaceCraft Control expression and modify the Realism value.
It should stay above 0.1, especially for smaller ships and doesn't really need to be higher 1.
Its default value is 5, which provides good flying conditions.

It is possible to disable the display of the cockpit's elements by opening the SpaceCraft Camera Manager expression and changing the values under "Display".


If you want to use SCC on another prop, get the 3 expression2s from the expression2 folder and follow these steps:

1. Spawn the SpaceCraft Control expression2 on a ship made of a single prop.
It is possible to spawn the expression on another prop and connect its "Scin" to an entity marker so the ship doesn't have to be the prop the E2 is welded to.
The same principle applies to SpaceCraft Camera Manager expression2.
You will have to refresh the expression after connecting Scin.
If the Expression is spawned directly on the ship to control, "Scin" doesn't have to be connected.
Remark: The model must have a correct forward() direction (ex. EVE online models will fly in the wrong direction)

2: Spawn the SpaceCraft Input Manager somewhere close to SCC

3: Place the ship in upright position and spawn the SpaceCraft Camera Manager close to SCC and SCIM.
If the ship isn't in upright position when SCCM is spawned, it will stop executing.
When SCCM's initilialisation is finished, the ship can be moved without any problem.

4. Place an adv pod controller, Joystick module and Cam controller close to the expressions. Link all of them to a seat.

5. Connect SCC's "Controls" input to SCIM. This will create a new wirelink to SCIM.

6. Connect SCIM's "Pod" input to the pod controller. This will create a new wirelink to the joystick.

7. Connect SCIM's "Joy" input to the joystick. This will create a new wirelink to the pod.

8. Connect SCCM's "Controls" input to SCIM.

9. Connect SCCM's "Pod" input to the pod controller.

10. Connect SCCM's "Cam" input to the cam controller. This will create a new wirelink to the cam controller.

11. Refresh SCCM.

You can refer to the wire schematic included in the pack.


### Forum threads ###

http://www.wiremod.com/forum/finished-contraptions/27381-spacecraft-control-13-5-a.html#post244667

http://www.facepunch.com/threads/1124230?p=32212079#post32212079