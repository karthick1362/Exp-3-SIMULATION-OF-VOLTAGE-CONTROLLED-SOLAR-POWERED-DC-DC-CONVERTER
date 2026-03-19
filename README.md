# Exp-3-SIMULATION-OF-VOLTAGE-CONTROLLED-SOLAR-POWERED-DC-DC-CONVERTER

## Aim:

To simulate solar powered DC/DC boost converter using MATLAB Simulation for the output voltage control using P-I Controller.

---

## Software Tool Used:
- MATLAB 2014 or above  

---

## Modelling Parameters:

### Solar PV:

| S.No | Parameters | Value |
|------|-----------|------|
| 1 | Maximum voltage | 120V |
| 2 | Irradiance | 1000W/m2 |
| 3 | Temperature at STC | 250C |

---

### Boost Converter:

| S.No | Parameters | Value |
|------|-----------|------|
| 1 | Inductor, L | 100µH |
| 2 | Capacitor, C | 1000µF |
| 3 | Switching frequency | 25kHz |
| 4 | Load Resistance | 350 W |
| 5 | Duty cycle | 10% to 80% |

---

### Controller Parameter:

| S.No | Parameters | Value |
|------|-----------|------|
| 1 | Reference voltage | 100V to 300V |
| 2 | P constant | 0.01 |
| 3 | I constant | 5 |
| 4 | Time domain | Continuous |
| 5 | Switching frequency | 10kHz |

---

## Theory:

Closed-loop proportional-integral (PI) control is a widely used technique for regulating the output voltage in a DC-DC boost converter. It helps maintain a stable and accurate output voltage despite variations in input voltage, load current, and other operating conditions. Here's a step-by-step explanation of how closed-loop PI control works in a boost converter:  

## Circuit Diagram:
<img width="1908" height="983" alt="image" src="https://github.com/user-attachments/assets/3e9c547c-ba52-4e8e-abc1-4141254e281a" />

### Components of the Control System:

Boost Converter: This is the DC-DC converter responsible for increasing the output voltage.  

Reference Voltage (Vref): This is the desired or setpoint output voltage that you want to achieve and maintain.  

Feedback System: The feedback system measures the actual output voltage (Vout) using a voltage sensor or divider network and provides this information to the controller.  

Controller (PI Controller): The controller calculates the error (the difference between the reference voltage and the measured output voltage) and generates a control signal based on this error. The PI controller has two component  

---

## Tabulation:

## Case 1: Before Step Change

| Vref (V) | Vin (V) | Iin (A) | Ppv (W) | V0 (V) | I0 (A) | P0 (W) |
|----------|--------|--------|--------|--------|--------|--------|
| 350 | 100 | 2.0 | 200 | 350 | 0.6 | 210 |

---

## Case 2: After Step Change

| Vref (V) | Vin (V) | Iin (A) | Ppv (W) | V0 (V) | I0 (A) | P0 (W) |
|----------|--------|--------|--------|--------|--------|--------|
| 230 | 165 | 1.5 | 247 | 230 | 1.0 | 230 |

---

Proportional (P) Component: The proportional component generates a control signal proportional to the error. It helps reduce steady-state error and provides a quick response to changes in the error.  

Integral (I) Component: The integral component accumulates the error over time and generates a control signal that eliminates any steady-state error. It helps in dealing with long-term deviations from the reference voltage.  

By using a closed-loop PI control system, a boost converter can provide accurate and stable output voltage regulation, making it suitable for various applications, including power supplies and battery charging systems. The proportional and integral gains (Kp and Ki) need to be properly tuned to ensure good control system performance.  

---

## Procedure:

1. Open MATLAB  
2. From Simulink library browser, pick the following components  
   a. Solar Panel  
   b. Current and voltage measurement  
   c. MOSFET, Diode, Inductor and capacitor  
   d. RLC series load  
   e. Constant, subtract, PI controller and PWM generator  
   f. Slider, Scope, display  

3. Connect the Simulink library tools as shown in the circuit diagram.  
4. Connect the slider tool with the constant block used for the reference value.  
5. Set the parameters as per the required design.  
6. Simulate the work for the different reference voltage by sliding the slider.  
7. Note the input and output side parameters and tabulate it.  

---
## Output Waveform 
 <img width="1915" height="886" alt="image" src="https://github.com/user-attachments/assets/c7a32263-04d2-4a18-9210-815a843816c9" />

## Result:

Thus, the closed loop output voltage control of solar powered dc/dc boost converter using PI controller is simulated using MATLAB.

