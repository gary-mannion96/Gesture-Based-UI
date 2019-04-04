# Project Details<a name = "details"></a>

| Project Details   |     |
| --- | --- |
| **Course** | BSc (Hons) in Software Development  |
| **Module** |  Gesture Based User Interface Development |
| **Members** | [Derrick Conway](https://github.com/DerrickConway)<br/> [Gary Mannion](https://github.com/Gazza1996)|

## Brief
Develop an application with a Natural User Interface. There are a number of options available to
you and this is an opportunity to combine a lot of technology that you have worked with over the
past four years.

## Purpose of the application
The main purpose of our application is to implement basic gestures over the controller and have each specific gesture light up a specific led light colour.  Our project will involve the leap motion controller and having it connected with the arduino board using a Node JS library running some commands which will in turn lead to us using some hand gestures on the leap motion and being able to then send a signal to a circuit board with some led lights pinned to it which will ommit a colour for a certain gesture.

The application will be an experimental based idea showing how we can use these technologies to develop applications that involve using specific hand gestures. The idea of using the circuit board will the LEDs is to back up our idea that the hand gestures are being recognised by using different colours for each gesture.

## Research
We had a great choice of technologies to use for this project from our Gesture Based UI module. We used different technolgies during our labs in order to gain a small amount of knowledge as to how they work and also to give us some ideas for use in our project. The college had a range of tech that we could have used for example they had [Kinect](https://en.wikipedia.org/wiki/Kinect) , [Myo Armband](https://www.myo.com/) , and [Leap motion Controller](https://www.leapmotion.com/). We both had decided before any research that we would either be using raspberry pi and arduino or just arduino for our project as we both an in interest in the tech and wanted to use one of them in a project to gain some knowledge on them. As students we didn't want to invest too much on these tech as we can't afford too, so the arduino with the leap motion(which we can use from the college) was our best idea.

### First Idea
- Our first idea we thought out was using an arduino and having a camera plugged into it and by using this camera we would be able to recognise some different hand gestures or movements.

### Second Idea
- After more research and learning about how the Leap Motion works we decided to go down a different path. We would be keeping our arduino but get rid of the camera plugin and instead use a breadboard for our lights while our Leap Motion would be detecting our hand gestures.

## Gestures identified as appropriate for this application
After researching the Leap Motion controller we discovered that the controller supports various hand gestures which in the end we decided to go with following:

![N|Solid](Images/hand-gestures.jpg)

Our main reason for choosing the above as the hand gestures for our project was that we believed these would be the most popular to be used in an application. 

- The swipe gestures is most popular in regards to moving between pages or controller the direction of an object
- The circle gesture could be incorporated into an application where a drag & drop feature is added or in a game wich requires you to throw something.
- The screenTap would be used in an app where you want to click on a button.
- The keyTap gesture can be used where we have an action where an app has a key press function.

Our objective here is to have all these gestures in our code and when one is performed a colour will light up for each one.

## Technology/Hardware Used

### Leap Motion Controller
The Leap Motion controller is a small USB peripheral device which is designed to be placed on a physical desktop, facing upward. It can also be mounted onto a virtual reality headset. Using two monochromatic IR cameras and three infrared LEDs, the device observes a roughly hemispherical area, to a distance of about 1 meter. The LEDs generate pattern-less IR light and the cameras generate almost 200 frames per second of reflected data. This is then sent through a USB cable to the host computer, where it is analyzed by the Leap Motion software using "complex maths" in a way that has not been disclosed by the company, in some way synthesizing 3D position data by comparing the 2D frames generated by the two cameras.

![N|Solid](Images/leap_motion.jpg)

- Download the SDK from https://www.leapmotion.com/setup/linux; We are using the Linux version as we are creating the project on a linux machine. Downloads are also available for Windows and MAC.
###### Note: The following is for on Linux machines only.
- Once the download is completed you will be asked to extract the files to a location and will see two DEB files in the folder.
- Open your terminal on the location of this folder and you must install the DEB files by using the following command:
```
sudo dpkg --install Leap-*-x64.deb
```
###### Note: 64 bit machines only.

### Arduino
- Arduino is an open-source physical computing platform based on a simple I/O board and a development environment that implements the Processing/Wiring language. 

![N|Solid](Images/arduino.jpg)

- You can download the Arduino IDE [Here](https://www.arduino.cc/en/Main/Software)

- For users on a Linux machine I would suggest watching the following video [Arduino IDE on Linux](https://www.youtube.com/watch?v=wh6StlwDBo0). It will go through how to properly install the IDE and it deals with any errors you should come across.

- When the IDE is successfully installed you must then flash your arduino board using the StandardFirmata example.
1. File->Examples->Firmata->StandardFirmata
2. Double-check that your arduino board is connected to the port(Tools->Port)
3. Once all is correct press the upload button(the right arrow button)
4. Should any errors arise when uploading refer to the video above(Arduino IDE on Linux)

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/ScreenS/Screenshot6.png">

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/ScreenS/Screenshot7.png">


- If Standard Firmata fails to load just return the commands in the third terminal and run the StanderedFirmata file again,
and it should work fine.

### BreadBoard Circuit
- Breadboard is retangular piece of plastic with a grid of holes that allows you to easily and quickly build an electronic circuits by pushing electronic components into the holes. Here is a similar one to one we used with come leds plugged into showing what we hope to implement.

![N|Solid](Images/breadboard.jpg)

## Architecture for the solution
From above we have our research section with our two ideas for the project. Below we have a diagram showing the architecture of our project clearly showing how everything will be connected up from our leap motion right around to our breadboard circuit.

![N|Solid](Images/architecture.png)

## Technologies Assembled
<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/Images1/view.jpg" width="350" height="350">

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/Images1/view1.jpg" width="350" height="350">

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/Images1/view2.jpg" width="350" height="350">


## How To Run
1. Install [Node](http://www.nodejs.org/)
2. ``` npm install ``` on your machine
3. Install [cylonjs](https://cylonjs.com), a robotics framework for JavaScript applications.
4. Make Sure your Leap Motion SDK is installed from above.
5. Using the ``` npm install ```  make sure to download, ``` npm install Cylon ```, ``` npm install cylon-firmata```, ```npm install cylon-leapmotion```

## Terminal Commands

- Alright after you have everthing installed you need to do the following to get it up and running.
- You need to clone it down from github to your desktop and click into the file you just downloaded. 
when in the file right click in it and open terminal but select as root terminal not the standard terminal.
And run ``` leapd ``` as shown below.

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/ScreenS/Screenshot2.png">

- Next you need to open a second terminal in the same file and run the follwing command,  ``` LeapControlPanel ``` as shown below.

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/ScreenS/Screenshot3.png">

- Now you should see a new green icon on the bottom of your toolbar menu, right click on it and select ``` Diagnostic Visualizer ```
and you should be greeted with this screen as showing below.

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/ScreenS/Screenshot4.png">

- Now we need to connect to the Arduino you need to open a third terminal. You just need to right click on the folder on the desktop and select treminal and run the followinng commands, ``` sudo chmod a+rw / dev/ttyACM0 ``` then enter your password if you are using linux.
and finaly run ``` node lm.js ``` as this is the name of the javascript file.

<img src="https://github.com/Gazza1996/Gesture-Based-UI/blob/master/ScreenS/Screenshot5.png">

## Demo Video

## Conclusion

For the conclusion we are going to list them as pros and cons of the project.

 Pros:
- Demonstrates how the Leap Motion controller can be used in web applications.
- Any issues were easily fixed as other people has the same problems.

 Cons:
- Can occasionally be glitchy when performing gestures. 
- Arduino configurations can sometimes throw up errors.


## References
- https://cylonjs.com/documentation/examples/cylon/js/leap_arduino/
- https://cylonjs.com/documentation/platforms/arduino/
- https://support.leapmotion.com/hc/en-us/articles/223782608-Linux-Installation
- https://www.arduino.cc/en/Guide/HomePage
