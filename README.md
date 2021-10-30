SELF BALANCING BOT

Self-balancing robot is a two-wheeled robot which balances itself so that it prevents itself from falling.

To keep the robot balanced, the motors must counteract the robot falling. This action requires feedback and correcting elements. The feedback element is the MPU6050 gyroscope + accelerometer, which gives both acceleration and rotation in all three axes. This value is passed through a Complimentary Filter to refine the data. The Arduino uses this to know the current orientation of the robot, and hence calculate how tilted the robot is from Vertical. 
The angle between current orientation and desired orientation gives us the error. The error value is fed into PID control system which as a result gives back PWM for motors. Finally this PWM is fed into the motors. Therefore correcting element is the motor and wheel combination.
