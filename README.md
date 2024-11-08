<!-- 
<table>
<tr>
<th width=250>
CONTENT
</th>
</tr>
</table>
-->




<div style="display: flex; flex-direction: column; align-items: center; justify-content: center;"
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;">







<h1 align = center> Future Engineers 2024 </h1>
<h2 align = center> Team Name: FASTGEAR </h2>
<h2 align = center> Team Members: Cem Onat KAYA, Kamil Poyraz UÇAR </h2>
<h2 align = center> Email: fastgear.fe2024@gmail.com </h2>


<p align="center">
  <img width="500" height="500" src="https://github.com/user-attachments/assets/48b12469-f676-4d16-961a-683ca4692622">
</p>

# <hr/>

# Contents 
* [**Mobility Management**](#mobility-management)
* [**Power and Sense Management**](#power-and-sense-management)
* [**Obstacle Management**](#obstacle-management)
* [**Robot Photos**](#robot-photos)
* [**3D Model**](#3D-model)
* [**Team Photos**](#team-photos)
* [**Videos**](#videos)
* [**Engineering Factors**](#engineering-factors)


# <hr/>


# Mobility Management

### Steering and differential design
We have a differential in the back of our robot. This allows our robot to distribute power to the wheels while enabling them to rotate at different speeds, particularly during turns to make turns smoother. This increases our robots stability, while also improving traction and handling. Our robot is controlled by steering and differantial mechs.


<img width="629" alt="Ekran görüntüsü 2024-09-16 211717" src="https://github.com/user-attachments/assets/db58cb6f-72cc-42dd-8fcb-cdbeb753e668">
<img width="633" alt="Ekran görüntüsü 2024-09-16 211859" src="https://github.com/user-attachments/assets/28826af2-b9b5-4f9f-a867-de64442156df">



### Weight distribution
  Because of our motors and large wheels being behind the center, our robot weight is  a little behind the center, and our robots center of gravity is low. This allows our robot to not topple, be much more stabile and take the turns easier.



  
### Camera position
  Our camera is positioned as high and far back as possible. This allows our robot to have a much  bigger cone of vision. Because our robots cone of vision is larger, our robot can manage obstacles much more efficiently. It is also tilted slightly downward to monitor 
  nearby blocks and improve obstacle handling.



  
### Motor selection
  We have a choice between 2 types of LEGO motors: large motor and medium motor, the large motor is powerful but the speed is lower, the medium motor is not that powerful but have a great speed. Because the category needs speed not power, we chose that it would be better to choose the medium motor type.
  We thought that the mobility that 1 motor gives us may not be enough so we combined 2 with a differential.


# <hr/>


# Power and Sense Management
## Power Management </br>
  The power source of our robot is the <a href="#">EV3 Programmable Brick</a>, it has a rechargable 10V Lithium Battery. EV3 P-Brick have 4 ports for motors and 4 ports for sensors. For the power consumption of motors and sensors: <a href="https://www.dexterindustries.com/ev3-current-consumption-measurement/">https://www.dexterindustries.com/ev3-current-consumption-measurement/</a>.
  <table>
<tr>
<th width=500>
  
  ![alt text](https://github.com/user-attachments/assets/7901a669-6c09-4c31-ba08-9381b82f198a)
</th>
</tr>
</table>

## Sense Management
  We used the ultrasonic, color and gyro sensors of the LEGO EDUCATION MINDSTORMS EV3 Core Set for the sense management of the robot.

  The ultrasonic sensors we used are very important on our open round codes ultrasonic sensors allow the robot to be equidestant from both walls and stay in the middle of the lane.
  Our gyro sensor is helping us calculate the error of the robots placement and fixing it.
  The color sensors help us see the colored lines that are in 4 corners of the area. Through this we can understand which way our robot should go, whether it should turn left or right and our robot can finish the track without having issues.

# <hr/>
# Obstacle Management

To go around the obstacles, our robot looks at x and y coordinates of the obstacles and looks ath the color of the obstacles. To do this we used the PixyCam. The code uses the x and y coordinates of the obstacle according to where it is placed on the cam and the color learning ability helps us with the paths the robot should take.

![alt text](https://github.com/user-attachments/assets/b257af2f-facd-4b6f-86b5-3247d9d6c7da)
## Open Race
We first start by making our steering mechs angle 0. Through this we can make our robot start in a straight line, and then we reset our motor rotation and gyro sensor's value. Our robot first checks if there are any colored lines, if there aren't, the robot starts to move. When it reaches the lines at the corners of the area, Through its color sensor, it can understand whether to turn clockwise or counterclockwise. Sometimes color sensor detects wrong color values. Because of this we made it so if our color sensor detects:

Red => it turns clockwise

Yellow => it turns clockwise

Brown => it turns clockwise

Blue => it turns counterclockwise

Black => it turns counterclockwise

After our robot turns, code increases the variable called "rounds" by 1. When this variable reaches 12, this means our robot finished 3 rounds. While our robot is not detecting any lines, It tries to center the lane. It does this using the "rotation" variable. Rotation variable increases by 30 if our robot is closer to the wall than 20 cm. if rotation variable increase, our robot starts to move away from the wall. When the rounds reaches 12, Our robot increases its speed and turns to the lane for 3 rotations, this allows our robot to finish in the lane.

## Obstacle Race
The code for the obstacle race is mostly the same as the code we used in open race. But there are differences. First of all, because we are trying not to hit obstacles, We sacrifice the robots speed in order to navigate around the obstacles better.
Second of all, before checking if there are any colored lines, our robot uses the pixycam to see if there are any obstacles. If there are, our code uses PID to center the obstacle, Because we center the obstacle pixycam will be able to identify the color of the obstacle without issues. After pixycam identifies the color, if the color is red: It turns right. If the color is green: It turns left. Robot continues turning until it cant see the color that it saw. While all of this is happening, our robot periodically checks if it detects any colored lines.


# <hr/>
# Robot Photos
![alt text](https://github.com/user-attachments/assets/8d8d52ca-e757-40a6-97bf-7d89b446d83c)
![alt text](https://github.com/user-attachments/assets/2a5b7c1e-2ac0-4eb2-8f36-c8f4e1c5c156)
![alt text](https://github.com/user-attachments/assets/19544f85-f2e9-49b1-8597-95eafcc71a36)
![alt text](https://github.com/user-attachments/assets/40ab5aa6-1ee3-48f6-89a9-0f42e0fdba8f)
![alt text](https://github.com/user-attachments/assets/e12f1cfc-711b-4aab-ab1f-f59345dc9b33)
![alt text](https://github.com/user-attachments/assets/7c6ef78b-b05e-44dc-9790-8439ca8926bf)
# <hr/>


# Team Photos
![alt text](https://github.com/user-attachments/assets/601c4a8b-9edf-4e55-9a91-7bce6154b8ab)

## (FUNNY)
![alt text](https://github.com/user-attachments/assets/eb73d4ad-773c-413c-bc0b-600fd81e9d27)

# <hr/>

# Videos
WRO Future Engineer 2024: Future Inside Open Challange: https://www.youtube.com/watch?v=YE7ToXtUVc4

WRO Future Engineer 2024: Future Inside Obstacle Course: https://www.youtube.com/watch?v=hPcQB7C0rqA

# <hr/>

# Engineering Factors
### Building The Robot
 We built the robot with LEGO. For the motors, sensors and the EV3 programmable brick we used the LEGO MINDSTORMS set. For the rest of the robot we combined LEGO MINDSTORMS set with LEGO Spike Prime set.

 To process the colors of the obstacles we used the PixyCam. The camera is a powerful tool with I2C communication protocol. It can distinguish the colors ,sizes and x, y coordinates of the obstacles. It also has a program (PixyMon v2) for the config of the Cam.

# <hr/>
# 3D Model
We 3D printed this model for connect the PixyCam to our robot.

![0c16bcc67fb93e3b44f921102f7a36db_display_large](https://github.com/user-attachments/assets/dc579fcb-9b1f-4756-875f-1cb5b07d6da2)


# <hr/>





### Coding The Robot
  For the code we used <a href="">LEGO MINDSTORMS</a> application.


<hr/>






