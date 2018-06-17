# Troubleshooting

## Clamp LED lights don't turn on when running the cavicapture.py script

* Check all the connectors. If you are using molex type connectors then make sure the pins are sitting properly and fixed in their housing.
* Check the continuity of connections using a multimeter.
* Check the 12v power supply is supplying voltage in the range 11.5 to 13.5.

## Preview window is blank (but captured images are fine)

* The resolution of the monitor is most likely too low to generate the preview which is set to the highest setting by default. In the cavicapture.py script change this line (~line 44):

  ``` 
  camera = picamera.PiCamera(resolution=(2592, 1944), framerate=15)
  ```

  to

  ``` 
  camera = picamera.PiCamera(resolution=(1920,1080), framerate=15)
  ```
