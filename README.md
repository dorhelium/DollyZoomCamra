# DollyZoomCamra
This program is a simulated 35mm autofocus dolly zoom camera. The camera provides the ability to select focus point, set sperture size, automatically adjust focal length according to the focus point, and create bizarre dolly zoom cinematic effect. The scene is rendered by averaging multiple renders with the accumulation buffer, and the users can set how many renders to be used.


 <img src="/dolly.gif">

## Instruction
The project uses Java and the JOGL openhl bindings.
Download the code and add the jogl, vecmath, and mintools jars to the root level of the project folder.
The utility files came from the 2.3.2 release folder (https://jogamp.org/wiki/index.php/Release_2.3.2) on the jogamp site. The fat jar contains all the necessary dlls and shared objects to work on all common platforms.

## Contents
This program contains folowing classes:
### CamApp 
Creates the canvases for two different camera views.
### Accum
Provides an emulated accumulation buffer.
### CanvasCam2 
Draws the sceen from a second camera, ie. a vizualization of the primary camera.
### CanvasDOFCam 
Draws the scene from the primary camera with depth of field effect.
### DOFCamera 
Defines the depth of field camera, including a number of different features, such as shifted perspective projections, dolly zoom and dolly focus.
### FastPoissonDisk 
Generates nice random but well distributed samples for sampling the aperture.
### Selector 
A class for selecting points in an image and converting them to world coordinates.
### Scene 
This is a simple test scene. However, this program works for any 3D scene.



