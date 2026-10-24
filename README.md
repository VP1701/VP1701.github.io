# Veeti Pekonen — Control Systems & Robotics
I'm a master's student in automation engineering at Tampere university, graduating in December 2026. Since 2024 I have worked as a research assistant at IHA-laboratory, developing control systems for a full-size electric wheelloader. My work has covered data callection, modeling, controller desing, systems desing and field testing. In my master's thesis I develop an optimization based algorithm for safe shared control of wheelloader, which prevents the user from colliding with obstacles while being minimally invasive.

Outside work I have personal projects which nclude ongoing projects like my C++ "control_toolbox" and camera turret and old projects like a drone I built at the start of my studies.

## control_toolbox
In this project I have developed optimization and control algorithms like QP-optimizer, PID and MPC in C++ without using external libraries like Eigen or libraries with ready optimization algorithms. In the project I have implemented everything from basic linear algebra to working MPC algorithm which supports linear and quadratic costfunctions. Currently I'm working on optimizing the MPC-algorithm. 

### WIP MPC control of quadcopter
In this project I develop position control for a quadcopter. This means that the controller would be the outer control loop on a real quadcopter. The first iteration uses a state space model linearized around hover and it is controlled with QP-MPC and tested in simulation. The benefit of MPC over more classical methods like PID or LQR is that MPC can incorporate constraints to inputs and states, which can increase reliability and performance in situations where the quadcopter is operated near its operating limits.

The current model has state vector x = [px, py, pz, vx, vy, vz, phi, theta]^T and 
inputs u = [phi_r, theta_r, T_r]^T, where T_r is thrust relative to hover. I assume that attitude is controlled by a low level controller which can be modeled as first order system.

[link to branch](https://github.com/VP1701/control_toolbox/tree/drone_test)



### Double integrator system test and matlab comparison
![MPC comparison plot](images/mpc_comparison.png)
*Comparison of my MPC algorithm with QP and LP costs against MATLAB's MPC with a QP cost.*

The repository can be accessed [here](https://github.com/VP1701/control_toolbox)

## Servo turret




## Quadcopter
I have built my own quadcopter in 2024. In this project I learned the basic components needed in a quadcopter and in general working with electronics, soldering etc.

## Openclaw agent