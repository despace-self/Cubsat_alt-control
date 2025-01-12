# Cubsat_alt-control
# CubeSat Attitude Correction Using PID Control

This repository contains a Python simulation of CubeSat attitude correction using PID control. The simulation incorporates a detailed model of CubeSat dynamics, external disturbance torques, and a feedback control system to maintain stability. The project is intended to serve as a foundation for understanding spacecraft attitude dynamics and control.

---

## **Key Features**

1. **CubeSat Dynamics:**

   - Moment of inertia calculated using CubeSat mass and dimensions.
   - Dynamics modeled as a second-order system.

2. **Disturbance Torques:**

   - Gravity Gradient Torque
   - Aerodynamic Drag Torque
   - Solar Radiation Pressure Torque

3. **PID Control:**

   - A PID controller with adjustable \(K_p\), \(K_i\), and \(K_d\) parameters.
   - Simulated step response for system stability and disturbance rejection.

4. **Visualization:**

   - Plots comparing system response with and without disturbances.
   - Animation of CubeSat attitude correction over time.

---

## **Equations Used**

### **1. CubeSat Dynamics**

The rotational dynamics are modeled as:

\[ J\ddot{\theta} + c\dot{\theta} = \tau_{net} \]

Where:

- \(J\): Moment of inertia
- \(c\): Damping coefficient
- \(\tau_{net}\): Net torque applied to the system

### **2. Disturbance Torques**

#### Gravity Gradient Torque:

\[ \tau_{gg} = \frac{3}{2} \cdot \frac{\mu}{r^3} \cdot (J_z - J_x) \cdot \sin(2\theta) \]

Where:

- \(\mu\): Earth's gravity parameter
- \(r\): Orbit radius
- \(J_x, J_z\): Moments of inertia
- \(\theta\): Angle of rotation

**Reference:**

- [Wertz, J. R. "Spacecraft Attitude Determination and Control"](https://www.springer.com/gp/book/9789400999053).

#### Aerodynamic Drag Torque:

\[ \tau_{drag} = 0.5 \cdot \rho \cdot v^2 \cdot C_d \cdot A \cdot l \]

Where:

- \(\rho\): Atmospheric density
- \(v\): Orbital velocity
- \(C_d\): Drag coefficient
- \(A\): Cross-sectional area
- \(l\): Lever arm length

#### Solar Radiation Pressure Torque:

\[ \tau_{srp} = \frac{P_s \cdot A \cdot l}{c} \cdot \sin(\theta) \]

Where:

- \(P_s\): Solar radiation pressure
- \(c\): Speed of light
- \(A\): Cross-sectional area
- \(l\): Lever arm length

**Reference:**

- [Solar Radiation Pressure and Satellite Dynamics - NASA Technical Reports](https://ntrs.nasa.gov/).

---

## **Simulation Details**

1. **Dependencies:**

   - Python libraries: `numpy`, `matplotlib`, `control`, `scipy`
   - Ensure `ffmpeg` is installed for animation saving.

2. **Code Workflow:**

   - Define CubeSat dynamics and disturbances.
   - Implement PID controller.
   - Simulate and visualize responses.

3. **Simulation Time:**

   - 1000 seconds with a resolution of 2000 time steps.

---

## **How to Run the Code**

1. Clone the repository:

   ```bash
   git clone https://github.com/your-repo/cubesat-pid-control.git
   cd cubesat-pid-control
   ```

2. Install dependencies:

   ```bash
   pip install numpy matplotlib control scipy
   ```

3. Run the simulation:

   ```bash
   python cubesat_simulation.py
   ```

4. View the animation (if generated):

   ```bash
   cubesat_attitude_correction.mp4
   ```

---

## **Future Work**

- Implement adaptive or optimal control strategies.
- Include 3D visualization of CubeSat attitude.
- Extend disturbance models for varying orbits.

---

## **References**

1. Wertz, J. R. "Spacecraft Attitude Determination and Control." Springer, 1978.
2. NASA Technical Reports - Solar Radiation Pressure and Satellite Dynamics: [https://ntrs.nasa.gov/](https://ntrs.nasa.gov/)
3. Orbital Mechanics Tutorials - [MIT OpenCourseWare](https://ocw.mit.edu/).
4. Fundamentals of Space Systems by Vincent L. Pisacane.

---

## **License**

This project is licensed under the MIT License. See the LICENSE file for details.

---

### **Author**

Deshad Senevirathne.

---

## Let’s Mine Space!

