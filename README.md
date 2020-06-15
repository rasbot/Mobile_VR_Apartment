# Mobile VR Apartment

As part of the Udacity VR Nanodeveloper degree, one of the first projects in Unity was to create a VR Apartment. This was a project that connected some of the more basic concepts of creating and interacting with a VR environment built in the Unity game engine and deployed to a mobile APK using the GoogleVR SDK. 

<img src="Images/VR_Apartment_CouchView.PNG" width="800" height="500"/>

Key concepts in this project include:

### Building environments

Games and VR experiences need worlds. Environments build in Unity consist of putting together assets, having skyboxes to enhance the intended mood, and giving the user things to explore an interact with. This project was one of the early projects to start building an environment, and an apartment setting was created.

<img src="Images/VR_Apartment_OutsideView.PNG" width="700" height="450"/>

### Locomotion

Mobile VR has only 3 degrees of freedom. The user can look left / right, up / down, and tilt their view of the environment. Modern VR systems such as the Oculus Rift or HTC Vive have 6 degrees of freedom which allows for translational motion in 3 dimensions along with rotational motion. For a mobile VR environment, some way of getting around is needed if movement within the game world is intended. One common approach to this is to use the click button of the VR headset to move to a specified waypoint. These waypoints are positioned around the environment and when the user looks at one and clicks the headset, they move to that position in the environment.

<img src="Images/VR_Apartment_Waypoints.PNG" width="700" height="450"/>

### Interactions and Animations

By using the Unity animation tool, a globe spin was animated and triggered by the click of the mobile VR headset. The Google VR viewer listens for a click which can be initiated on older mobile headsets as a magnetic "button" or the more recent headsets which essentially have a screen press as a button, and that click is used with `Animator.SetTrigger()` to play the animation once, spinning the globe. The user uses the waypoints to naviagate closer to the globe and can spin the globe using this process.

<img src="Images/globe_animation.gif" />