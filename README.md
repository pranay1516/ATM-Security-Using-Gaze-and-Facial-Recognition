# ATM Security Using Gaze and Facial Recognition

An OpenCV project for using the blinking of eyes as a password.

## Usage on Various Operating Systems

This eye blink password script will work on all OS: Windows, Mac, and Linux.

**Windows**: An Anaconda environment `.yml` config file has been provided for easy dependency installation.  
**Mac**: Dependency resolution currently must be performed manually.  
**Linux**: Dependency resolution also must be performed manually.  
If using this on a Raspberry Pi, search the Drone Dojo YouTube channel for the installation walkthrough.

## What This Script Does

See the YouTube video for a visual representation.

Some people type words for their passwords. This script is a proof of concept allowing you to blink your eyes as a password using OpenCV and a camera.

Example password: `'LRB'`  
Each digit can be:
- `L`: Left eye closed  
- `R`: Right eye closed  
- `B`: Both eyes closed

The password length can be as long as desired.

### To unlock the password:
1. Hold left eye closed, right eye opened  
2. Open both eyes (locks in the left eye closed digit)  
3. Hold right eye closed, left eye opened  
4. Open both eyes (locks in the right eye closed digit)  
5. Hold both eyes closed  
6. Open both eyes (locks in the both eyes closed digit)

When the full sequence is entered correctly, the script exits or performs the unlocking logic.

## Eye Blink Safe

An example application of this project is the Drone Dojo 'Eye Blink Safe'.

The safe is powered by a Raspberry Pi. When the password is matched, the code triggers a solenoid lock to open a 3D-printed safe.

If you're using this for the Eye Blink Safe, make sure to set the `isEyeBlinkSafe` variable in the script to `True`.

The Eye Blink Safe also uses an LCD screen to display relevant information from the script to the user.
