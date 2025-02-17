# LIC-LAB_Aneesh_kulkarni
Given that the power, P = 100µW, conduct DC Analysis, Transient Analysis, and AC Analysis for the specified circuit designs. Additionally, observe the impact of increasing or decreasing the width of each MOSFET on circuit performance
Circuit-1:
Aim:
![Screenshot 2025-02-17 222813](https://github.com/user-attachments/assets/2d6acf33-ec23-4834-be68-39c4b07bffac)
Using the power formula:
P=V*I
The drain current (Id) is determined as:
Id= 5.56 * 10^-5 A
To achieve the required output current (Id), adjustments are made to the length (L) and width (W) of the MOSFET channel. The specific channel dimensions used to obtain the given current are illustrated in the provided figure.
![Screenshot 2025-02-17 223309](https://github.com/user-attachments/assets/0184e91e-456f-4494-b527-75f4946d0225)
1) DC Analysis:
Procedure:
Open the Edit Simulation Command and choose the "DC Operating Point" (DC op pnt) option.
Run the simulation to obtain the required results.
![Screenshot 2025-02-17 223724](https://github.com/user-attachments/assets/3390899e-10a6-42b2-9e5c-0e29e3171e26)
Observations:
The DC analysis results confirm that the drain current aligns with the expected value of 5.56 * 10^-5A
The correct current was obtained by selecting suitable channel dimensions, with L = 180nm and W = 203nm.
The circuit demonstrates expected behavior under DC conditions.
<img width="344" alt="image" src="https://github.com/user-attachments/assets/531e1a0b-18d6-4cff-b2f8-320c9a9ba23d" />
2) Transient Analysis:
Procedure:
Select "Transient Analysis" in the Edit Simulation Command.
Set the stop time to 1ms.
Execute the simulation.
![Screenshot 2025-02-17 225401](https://github.com/user-attachments/assets/7e179fe7-cab6-4732-a208-8b4a27d28a4b)
Observations:
The transient response graph displays the circuit's time-dependent behavior.
The response is smooth, with no unexpected deviations or distortions.
The circuit reacts appropriately to input variations, confirming its stability
![Screenshot 2025-02-17 225531](https://github.com/user-attachments/assets/e6bcbb7d-845e-4869-801e-78c241acfdc6)
![Screenshot 2025-02-17 225745](https://github.com/user-attachments/assets/a0acd6ae-90f4-4fc5-9310-15ea94aa8e58)
3) AC Analysis:
Procedure:
Choose "AC Analysis" in the Edit Simulation Command.
Input the required values and run the simulation.
![Screenshot 2025-02-17 225949](https://github.com/user-attachments/assets/9c75ed90-b39f-4794-b791-e8f13b422f06)
Observations:
The AC response graph illustrates that the circuit remains stable across different frequencies.
The gain of 2 dB and phase shift (approximately 180°) align with theoretical predictions.
The circuit maintains stable performance throughout the tested frequency range.
![Screenshot 2025-02-17 230030](https://github.com/user-attachments/assets/0a06af5a-b99d-46a4-b05b-457ff532c11a)
Conclusion (AIM-1):
Properly selecting MOSFET dimensions enables effective control over the drain current.
Effect of Width Adjustments:
The width of M1 significantly influences Id, indicating its impact on output current.
The circuit operates effectively in all three analyses (DC, Transient, and AC), confirming its reliability.
The overall design follows theoretical expectations and is practically feasible.

Circuit-2
Aim:
To analyze the DC, transient, and AC characteristics of a Common Source (CS) amplifier circuit using LTspice and extract relevant parameters.
Components Required:
N-channel MOSFET (nmos4, pmos4), voltage sources (1.8V, 0.9V), and connecting wires.
Theory:
A diode-connected MOSFET operates in the saturation region and functions as both an amplifier and a current source. The three types of analyses performed are DC analysis, AC analysis, and transient analysis.
The drain current is given by the equation:
Id = 1/2 kn Vov2 ; Vov=Vgs-Vth and kn=un Cox W/L
DC Analysis helps verify that the MOSFET remains in the saturation region by examining its biasing conditions, ensuring it functions as an amplifier. Key parameters such as drain current (Id), gate-source voltage (Vgs), and drain-source voltage (Vds) are determined.
Transient Analysis evaluates the amplifier’s response to a time-varying input signal, such as a sine wave. This analysis provides insights into the time-domain behavior, including output signal amplitude and phase shift.
AC Analysis determines the voltage gain of the amplifier. The voltage gain for a common-source amplifier is expressed as:
Av=-gmRD
where gm represents the transconductance of the amplifier.
Procedure:
Step 1: DC Analysis
Construct the circuit in LTspice, incorporating the MOSFET, resistors, and supply voltage (Vdd).
Assign the MOSFET model as CMOSN and define its length and width.
Use the .op command in LTspice to perform DC operating point analysis.
Record values for drain current (Id), gate-source voltage (Vgs), and drain-source voltage (Vds).
Step 2: Transient Analysis
Introduce an AC signal source (Vin) at the MOSFET’s gate.
Apply the .tran command in LTspice for transient simulation.
Configure simulation time and time step (e.g., 10ms).
Observe the output waveform to analyze the time-domain response, including amplitude variations and phase shift.
Step 3: AC Analysis
Replace the DC signal source with an AC voltage source (small AC signal, e.g., 1V).
Utilize the .ac command in LTspice for frequency response analysis.
Set a frequency range, such as 1 Hz to 10 MHz, to evaluate gain and phase characteristics.
Examine the frequency response to determine gain and bandwidth.
Circuit Diagram:
![WhatsApp Image 2025-02-17 at 23 45 21_d691f325](https://github.com/user-attachments/assets/d37177b5-89e0-4fdb-9d02-826e31051ecf)
Calculations:
Power = 100uW

P = V*I ; ( V= 1.8 V)\
That implies I<sub>d</sub> = 55.55uA

V <sub>out/sub> = 1.664 V

Length= 180nm

Width=0.88um

V<sub>ds</sub> = V<sub>out</sub>
## Tabular Column:

|Width  |  Current(Id) |  Vout |
|:----: |  :---------: |  :--: |
|1.0um  |  61.27uA     | 1.667 |
|0.5um  |  56.63uA     | 1.665 |
|0.8um  |  52.00uA     | 1.661 |
|0.88um |  55.55uA     | 1.664 | 

Simulation Results:
DC Analysis:
![Screenshot 2025-02-17 234750](https://github.com/user-attachments/assets/bf581e01-42ca-458b-b9e3-c4eb6aa8606c)
DC Operating Point =( 1.664V ,55.55uA)
Transient Analysis:
![Screenshot 2025-02-17 234851](https://github.com/user-attachments/assets/a48a394e-1840-4554-827a-b355e46cbbad)
There is 180 degree phase shift between input and output. Vout=1.664V and the width =0.88um.

AC Analysis:
![Screenshot 2025-02-17 234931](https://github.com/user-attachments/assets/e78faaba-ecb3-4954-b7e1-5281609a10df)
Gain = -0.85 dB
Inference:
The drain current increases proportionally with MOSFET width, demonstrating its dependence on device dimensions.
The MOSFET operates in the saturation region, ensuring stable Q-point conditions for linear amplification.
Transient analysis highlights the circuit’s time-domain response and ability to adapt to variations in input signals.
AC analysis confirms that gain and impedance matching are essential for circuit design based on desired performance specifications.
