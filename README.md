# IronManVRFlightUnity
Proof of concept in Unity which allows you to fly around like Iron Man using the Oculus Touch controllers. When the trigger buttons are depressed, the script calculates where the controllers are relative to the headset and applies a force on a parent RigidBody which the camera is attached to. The script also controls particle and sound effects when thrusting. This is meant just for fun and won't be further developed.

**Tested on an Oculus Quest**

**NOTE:** You probably shouldn't actually use this. I had no idea what I was doing with this and the concept is simple enough where you should just do it over and use this as reference.

## Steps to recreate
1. Create a rigidbody and freeze all rotation
2. Add OVRCameraRig as child to rigidbody
3. Add LocalAvatar as child of OVRCameraRig
4. Add CustomHandLeft and CustomHandRight as children to OVRCameraRig (I did a separate LocalAvatar since CustomHands on HandAnchors were jittery, hopefully you can do better)
5. Add particle effect to LeftHandAnchor and RightHandAnchor
6. Add HandThruster.cs as script to top level rigidbody
7. Hook up all the variables to the HandThruster.cs script (Should be straight forward)
8. Cross fingers and deploy to device

## TODO:
* Use orentation of hands as input to thrust instead of location relative to headset
