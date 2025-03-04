# Experiment-03: Differential Amplifier


## Differential Amplifier

This report provides comprehensive insights into the differential amplifier, detailing its theory, circuit design, working principles, and applications.

### CONTENTS

* Introduction/Theory of Differential Amplifier
* Circuit Diagram with Specifications
* Working Principle and Types of Differential Amplifiers
* Analysis of Circuit Design and Questions
* Role of Each Component & Steps for LTSpice
* Frequency Response and Gain Calculation
* Applications of Differential Amplifier
* Circuit Diagram Simulation Results
* Results, Inferences, and Conclusion
* References

### INTRODUCTION/THEORY

A differential amplifier amplifies the difference between two input signals while rejecting any common-mode signals. By replacing resistors with MOSFETs in the differential amplifier circuit, the gain is increased, although this may reduce the area and power efficiency. Differential amplifiers are integral to operational amplifiers (op-amps) and are essential for signal processing, noise reduction, and sensor interfacing. The circuit consists of two MOSFETs that amplify the difference between two input signals while rejecting common-mode noise. Essentially, a differential amplifier combines inverting and non-inverting amplifiers.

#### Diagram of an Operational Amplifier as a Differential Amplifier

A differential amplifier using an op-amp can be represented by the equation: \[ V_o = A_d (V_1 - V_2) \]

The voltage difference between the inverting and non-inverting terminals is amplified, resulting in an amplified output. Due to their input configuration, all op-amps are considered differential amplifiers. When two inputs are applied to the terminals, the resulting voltage difference is proportional to the difference between the two input signals. The differential amplifier acts as a subtractor circuit, essentially subtracting one input signal from the other. Differential amplifiers can be constructed using BJTs, FETs, and MOSFETs.

### CIRCUIT DIAGRAM WITH REQUIRED COMPONENTS & SPECIFICATIONS

In integrated circuits (ICs), fabricating high-value capacitors is challenging. Therefore, in amplifiers, capacitors are often replaced without losing their effect. This is achieved using differential amplifiers.

* Power Supply (Vdd): 3.2V
* Input Voltage (Vicm): 1.6V
* Drain Resistors (Rd1 = Rd2 = Rd): 3.48K
* Rss: 0.68K
* Output Common-Mode Voltage (Vocm): 1.7V
* Node Voltage (Vp): 0.6V
* Ground: 0V

![Circuit Diagram](https://github.com/user-attachments/assets/a4a89b43-9b69-4de0-9994-87b0e2f803a6)

The differential input voltage is given by: \[ V_1 - V_2 = V_d \]

The output can be either differential-ended or single-ended. Ideally, if ( V_1 = V_2 ), the output will be 0V. The input voltages can be expressed as: ![](https://mistralaichatupprodswe.blob.core.windows.net/chat-images/tool/ba/51/f7/ba51f7e5-bd13-4002-a1ce-62383ad78b4d/31175bf3-1c36-4962-808c-84a6f9d966bc/ba15b73e-2774-496a-8f16-5903485230d0/__emitted_0.png?sv=2025-01-05&st=2025-03-04T19%3A29%3A35Z&se=2025-03-04T20%3A29%3A35Z&sr=b&sp=rade&sig=bt7AvNQ2ygckAEphXxFh5E4rNnovKLVnEe3%2Bnuq40oI%3D)

Similarly,

![](https://mistralaichatupprodswe.blob.core.windows.net/chat-images/tool/ba/51/f7/ba51f7e5-bd13-4002-a1ce-62383ad78b4d/31175bf3-1c36-4962-808c-84a6f9d966bc/901eed5a-b0bd-430b-991d-bb02ef9799e5/__emitted_0.png?sv=2025-01-05&st=2025-03-04T19%3A27%3A14Z&se=2025-03-04T20%3A27%3A14Z&sr=b&sp=rade&sig=iYkhGZ9Ni%2FFhVZR8FCmca3I4qeAv0rDQ7yqJOsbQBxI%3D)

From these equations, we derive: ![](https://mistralaichatupprodswe.blob.core.windows.net/chat-images/tool/ba/51/f7/ba51f7e5-bd13-4002-a1ce-62383ad78b4d/31175bf3-1c36-4962-808c-84a6f9d966bc/6512da7e-2e3e-49c4-88fd-dfb4103084de/__emitted_0.png?sv=2025-01-05&st=2025-03-04T19%3A30%3A51Z&se=2025-03-04T20%3A30%3A51Z&sr=b&sp=rade&sig=9zGyQ%2BV6LH4EpnrpyCvDhZNCK3zx%2FI6yiiyO7uE08sI%3D)

Thus, ![](https://mistralaichatupprodswe.blob.core.windows.net/chat-images/tool/ba/51/f7/ba51f7e5-bd13-4002-a1ce-62383ad78b4d/31175bf3-1c36-4962-808c-84a6f9d966bc/8269d53b-9f72-4d62-af48-78bd92c88800/__emitted_0.png?sv=2025-01-05&st=2025-03-04T19%3A33%3A04Z&se=2025-03-04T20%3A33%3A04Z&sr=b&sp=rade&sig=a5UN5WBD%2BL78XhHv8UUbxt2OC%2Fqki3pVreTCIDJbryA%3D)

### Key Points About Common Mode and Differential Mode Analysis

#### Common Mode Signal

When both inputs of the differential amplifier receive the same signal, it is considered a common-mode signal.

#### Differential Mode Signal

When the inputs receive different signals, it is considered a differential-mode signal. A good differential amplifier should have a high Common-Mode Rejection Ratio (CMRR), significantly amplifying the differential-mode signal while rejecting common-mode noise.

### Analysis

#### Common Mode Analysis

Calculate the output voltage when the same input signal is applied to both input terminals of the differential amplifier.

#### Differential Mode Analysis

Calculate the output voltage when two different input signals are applied to the input terminals of the differential amplifier.

### WORKING PRINCIPLE

For proper amplification, the differential amplifier operates in the active region and can function in different modes: common-mode (same signal on both inputs) and differential-mode (different signals on inputs).

 1. The output is affected by the resistors (Rd): ( V\_{out} = V\_{dd} - I_d \\times R_d ).
 2. The circuit is designed symmetrically, ensuring equal current distribution.
 3. It receives two input signals and compares them.
 4. It amplifies only the difference between the two inputs.
 5. Any noise or interference present in both inputs is removed.
 6. Both transistors share the same power source and work together to balance the signals.
 7. The input signals control the current split between the two transistors, determining the output.
 8. The output changes based on the difference between the input signals.
 9. Feedback is often used to stabilize gain and improve performance.
10. Both transistors or MOSFETs work in a balanced manner, reducing errors due to temperature changes.

### TYPES OF DIFFERENTIAL AMPLIFIERS

1. **Resistive Load Differential Amplifier**: Uses resistors as loads (simple but low gain).
2. **Active Load Differential Amplifier**: Uses MOSFET loads for higher gain.
3. **Current Mirror Differential Amplifier**: Provides improved matching and increased gain.
4. **Fully Differential Amplifier**: Provides both differential inputs and outputs for better noise rejection.

### ANALYZING THE QUESTION WITH PROPER FORMULAS

#### Design a Differential Amplifier for the Following Specifications

* Vdd = 3.2V
* P ≤ 2.8mW
* Vicm = 1.6V
* Vocm = 1.7V
* Vp = 0.6V

Perform DC Analysis, Transient Analysis, and Frequency Response, and extract the required parameters.

Given:

* Vdd = 3.2V
* P ≤ 2.8mW
* Vicm = 1.6V
* Vocm = 1.7V
* Vp = 0.6V

#### Values of Each Component

* Rd = 3.48K
* Rss = 0.68K
* Iss = 0.875mA
* Id = 0.43mA
* Vdd = 3.2V
* P ≤ 2.8mW
* Vicm = 1.6V
* Vocm = 1.7V
* Vp = 0.6V
* ![](https://mistralaichatupprodswe.blob.core.windows.net/chat-images/tool/ba/51/f7/ba51f7e5-bd13-4002-a1ce-62383ad78b4d/31175bf3-1c36-4962-808c-84a6f9d966bc/c4e3a3b3-0a43-42fa-9bac-6fc23ea6952e/__emitted_0.png?sv=2025-01-05&st=2025-03-04T19%3A24%3A00Z&se=2025-03-04T20%3A24%3A00Z&sr=b&sp=rade&sig=vG8XfH3BGF5v%2FD8Ok8FzEgGrTpF6Rh8pn4SzvFIAPKc%3D)

### ANALYZING THE CIRCUIT USING LTSPICE


| **PARAMETER INCREASED** | **EFFECT ON Rd** | **EFFECT ON Rss** | **EFFECT ON Vout** | **EFFECT ON Vin** | **EFFECT ON GAIN** |
| --- | --- | --- | --- | --- | --- |
| Vdd | No direct effect, but voltage across RD increases | No direct effect, but Iss may need adjustment | Increases (more headroom, higher swing) | No direct effect, but biasing may shift | Increases (higher VDD allows a larger RD) |
| RD ↑ | — | No direct effect, but affects current balance | Increases (higher gain, larger swing) | No direct effect | Increases (Av = -gm * RD) |
| RSS ↑ | No direct effect | — | Improves CMRR, but excessive RSS may reduce gain | Differential input range may reduce | Can improve CMRR, but too large RSS reduces gain |
| W (Width) ↑ | No direct effect, but higher gm reduces needed RD for same Av | No direct effect, but affects bias current | May decrease (if lower RD is used) | Increases input capacitance | Increases (since gm increases) |
| L (Length) ↑ | No direct effect, but increases output resistance | No direct effect | Can increase (better channel control) | No direct effect, but speed decreases | Increases slightly (higher output resistance) |
In simple terms:

* More VDD: More Vout, More Gain
* More RD: More Vout, More Gain
* More RSS: Better CMRR, but can reduce gain
* More W: More Current, Less Vout (if RD fixed), More Gain
* More L: More Gain, Better Output Resistance

### ROLE OF EACH COMPONENT IN THE CIRCUIT

* **M1 & M2**: Amplify the difference between inputs.
* **M3 (ISS Source)**: Provides a stable tail current after replacement.
* **M4 & M5 (Active Load)**: Replace resistors to improve gain after replacing RD with MOSFETs.
* **RD**: Converts current to voltage (affects gain).
* **RSS**: Improves CMRR but can reduce gain.
* **Biasing Circuit (VBIAS)**: Sets MOSFET operating points.

### STEPS FOR LTSPICE SIMULATION

1. Design the circuit in LTSpice as per the circuit diagram.
2. Set the input voltage as an AC source.
3. Run DC, Transient, and AC Analysis to observe current and signal amplification.
4. Verify the current and phase inversion in the waveform.
5. Replace Rss (R3) with a current source and follow the same procedure.
6. Replace the current source with a MOSFET and observe DC, Transient, and AC Analysis.
7. Replace Rd1 and Rd2 with MOSFETs and follow the same steps. Replacing these resistors increases the gain, which is the main advantage of these steps.

### DC ANALYSIS

![DC Analysis](https://github.com/user-attachments/assets/0db3dfd9-b2fd-4a00-b877-9e643d963033)

### TRANSIENT ANALYSIS

![Transient Analysis](https://github.com/user-attachments/assets/b4bdb08b-d146-47c8-a1df-6960ef73b312)

### AC ANALYSIS

![AC Analysis](https://github.com/user-attachments/assets/d47373d5-f0be-4c65-80ff-6414871a317b)

### REPLACED RESISTOR (RSS) WITH A CURRENT SOURCE (ISS)

![Replaced Rss with Iss](https://github.com/user-attachments/assets/f0ee53a8-b699-47e9-9029-6b550eff3532)

### DC ANALYSIS

![DC Analysis with Iss](https://github.com/user-attachments/assets/badf0034-32d8-423b-9fcb-9b4fef129275)

### TRANSIENT ANALYSIS

![Transient Analysis with Iss](https://github.com/user-attachments/assets/c8f6a61d-a717-4fcc-9062-dc455189f017)

### AC ANALYSIS

![AC Analysis with Iss](https://github.com/user-attachments/assets/52ae2cde-485f-4538-b1f4-d24dda0be620)

### ADVANTAGES

### REPLACED CURRENT SOURCE WITH A MOSFET

![Replaced Iss with MOSFET](https://github.com/user-attachments/assets/1acbb66a-6fcf-4a9e-8a00-c218f82bca33)

### DC ANALYSIS

### TRANSIENT ANALYSIS

![Transient Analysis with MOSFET](https://github.com/user-attachments/assets/0206307b-9589-4af4-8994-18f101411cfe)

### AC ANALYSIS

![AC Analysis with MOSFET](https://github.com/user-attachments/assets/98fb0bb8-28d4-490a-8e27-8ed34223ec95)

### REPLACE RD WITH MOSFET

![Replaced Rd with MOSFET](https://github.com/user-attachments/assets/3340a503-d272-472e-809e-54c775b8e765)

### DC ANALYSIS

### TRANSIENT ANALYSIS

![Transient Analysis with Rd Replaced](https://github.com/user-attachments/assets/b28f37c4-ce2b-45c0-af54-9d58b22751de)

### AC ANALYSIS

![AC Analysis with Rd Replaced](https://github.com/user-attachments/assets/1a3d2325-9c9f-40a5-9447-0ad37665d975)

### RESULT

### INFERENCE

The differential amplifier effectively amplifies differential signals while rejecting noise. The operating points are set as required values, and the CMRR is enhanced using current sources and active loads. MOSFET-based designs offer better power efficiency and high input impedance. The circuit is widely used in modern analog and mixed-signal designs to increase gain. However, a main disadvantage is the reduction in area and power efficiency.

### FINAL CONCLUSION

The differential amplifier is a fundamental circuit in analog electronics, crucial for applications in op-amps, instrumentation, and communication systems. With proper design, high gain, low noise, and excellent common-mode rejection can be achieved. Simulation and experimental results confirm its effectiveness in signal amplification and noise reduction.


