# TTVR Mobile Beta

_Short cheat sheet for the TTVR Mobile Beta_

## Data and scope
The content shows full boston with streets, green space and water as a flat map. The region of dorchester is displayed with extrudes and with two plans (North and south). The plans have three, relatively four scenarios. 

The heavly optimized demo has a max triangle count of ~600k (average 350k) and a max mesh draw call of ~150. The documentation guidelines from oculus aim at 50-100 drawcalls and 50k-100k triangles. Therefore some laags, reprojection frames and in the worst case crash's must be accepted. 

## Start of the application
_You can start the application over different ways:_
* Oculus Menu -> Library -> Unknown sources (left) -> TTVR Mobile (last item without scrolling)

_When connected to a computer:_
* Sidequest -> Currently installed apps (icon top right menubar) -> com.esri.zrh.xr.TTVR


## Guardian and controller
You only need one controller (right). Maybe the display shows a warning for "left controller not found".
Best experience is to create a guardian - either a roomscale or a standing experience. This because then the starting position inside the TTVR Mobile is defined. You can always re-center by press&hold the Oculus menu button (Quest function).







## Reduced or disabled features compared to Desktop
_Following features have been reduced or disabled:_
* Post process / Rendering Style controller
  * This includes outline effect on buildings (boundary not affected)
* Dynamic light laserpointer and ambientlight
  * UE/Vulkan/Mobile Android only supports one movable light. This is defined now to be the sun (for the directional dynamic shadows). Light at the end of the laserpointer is disabled. 
* Shadows
  * Mobile only supports 4 shadow cascades in total, so we introdced two for far shadows and two for the regular shadows. The distances are adjusted to the boston city and do not scale. 



## Known issues
_Due to the heavy requirements we have currently in this beta:_
* Small flickering of ground-mesh's which are wider than your FoV
* Generally a lower quality
 

## Onboarding reset
You can reset the onboarding by press&hold the grip-button (middlefinger) for five seconds. After release, the scene get's resetted and the onboarding starts again. (You still can cancel it with the close-icon)

