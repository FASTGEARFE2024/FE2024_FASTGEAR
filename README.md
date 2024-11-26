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
For open race we chose the Classroom application because we realized that the sensor's reading speed is very important in wall following, and we conducted a test. In this test, we increased the value of the variable X, initially set to zero, by 1 every second for 5 seconds using both the Classroom Application and the EV3-G program, and finally displayed the value of X on the screen. In this test, the code written with the Classroom application resulted in 33646, while the code executed with the EV3-G program resulted in 21732. This showed us that the EV3 responded faster with the code written in the Classroom application, and indeed we observed that it turned more quickly after reading the value from the Ultrasonic sensor.

At the start of the code, we either press left or right buttons of the hub. According to the button we press, we use different versions of the code. if we press left our robot turns clockwise and if we press right our code turns counterclockwise.

In our code we have a function called "TURN". First, we reset the degree of motor A. Motor A is our steering mech. Then we set our movement motors to B and C. After that we set the variable "round" to 0. Every time our robot does a turn in one of the 4 corners of the track, round variable increases by 1. When the round variable becomes 12, Our robot makes 1 more turn and then stops. if round variable is not 12, Then our robot does the "TURN" function.

Now we will define the TURN function. First our robot starts to move at 60% speed. Then, if the ultrasonic sensor 2/4 (The sensor that looks at the inner walls. If we press left sensor is 2, if we press right sensor is 4.) sees that the distance is more than 220 cm, it increases the round variable by 1. After that, we decrease our robots speed by 45% (making it 25%) to make the turn easier. Then, our steering mech starts to move at -/+45% power(- if we press right, + if we press left.) . This makes our robot's steering mech turn with nearly full power. Our robot continues to turn to right until ultrasonic sensor 2 sees that the distance is less than 200 cm.
When the ultrasonic sensor sees less than 200 cm, the steering mech stops. If ultrasonic sensor doesn't see 220cm as distance at first, it instead checks if ultrasonic sensor 2 sees less than 20 cm. if this condition is met, our robot runs motor A with -/+45% power until the degree of motor A is greater than 10 degrees. When motor A is greater than 10 degrees, motor A stops. If ultrasonic sensor 2 doesn't see less then 20 cm, robot runs motor A with -/+45% power until the degree of motor A is lower than 10 degrees. After that motor A stops.
![3e32662d-19e8-409a-87cb-9dde82bc2513](https://github.com/user-attachments/assets/84e3fed7-ddce-4476-a3d4-287402f26824)

## Obstacle Race
Even though we wanted to use EV3 Classroom rather than EV3-G, we used EV3-G to use Pixycam's code blocks.
In obstacle race, our code first resets gyro sensor. After that it sets a variable called "round" to 0. After that the code waits until we press left or right buttons on the hub. If we press left button, we move counterclockwise at corners of the lane. If we press right button we move clockwise at corners of the lane. Our code then checks if there are any visible obstacles, if it sees one, then it checks its position on the x axis. If its position is more than 128, it truns left for -15 degrees. If its position is not more than 128, it turns right for 25 degrees. Through this our robot centers the obstacle. Because we center the obstacle, our turns can be made easier. Our robot continues to center the obstacle until the visible area of the obstacle is more than 2500. Then, our robot checks if the obstacle that it sees is red or green. if its red, it turns left for 12.5 cm, goes straight for 5 cm and goes right for 12.5 cm. Through this, our robot always centers its lane. If the color of the obstacle is green, it turns right for 12.5 cm, goes straight for 5 cm and goes left for 12.5 cm.

If our robot did not see an obstacle, it centers itself and goes straight. Because there is a possibility that it deviates from its path, we use a PD with the gyro sensor.

If our robot sees blue or orange lines, This means that the robot is at one of the corners of the lane. When that happens our robot turns for 60 degrees. and every 20 degrees it checks if pixycam can see an obstacle.


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






