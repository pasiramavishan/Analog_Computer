# Analog-Computer

This is a group project done under the module EN2091 Laboratory Practice and Projects, Semester 3 of the Department of Electronic and Telecommunication Engineering.

1. Introduction
   
- This project delves into the practical application of operational amplifier (op-amp) circuits for fundamental analog computations of addition, subtraction and multiplication. Beyond these core functionalities, the project is enriched with several key features aimed at providing a comprehensive and user-friendly experience in analog signal processing.

2. Key Features

- Diverse Operations: Dedicated op-amp circuits are implemented for each fundamental analog computation, showcasing the versatility of analog electronics.
  
- Frequency Range: Handle dual-channel input interfaces within a wide frequency range which is from 1Hz to 10kHz, enabling the processing of various signal types.
  
- User-Friendly Controls: User-friendly control mechanisms are employed for adjusting gain and biasing, allowing users precise control over the amplifier's characteristics.
  
- Precision and Accuracy: Prioritize achieving high accuracy and precision in computed results by minimizing signal distortion, noise, and non-linearities.
  
- Adjustable Operation Mode: Dynamically switch between addition, subtraction, and multiplication modes using the control interface, providing adaptability for diverse signal processing needs.
  
- Stable Power Supply System: A reliable and clean power supply system is designed to ensure consistent operation of op-amp circuits, incorporating appropriate filtering and regulation techniques.

![Analog_Computer](https://github.com/NilupuleeA/Analog-Computer/assets/153465850/b66c465d-21d6-482b-95f7-0a090533c900)

What you can find here:

- Simulation Files
- Schematic Diagrams
- PCB Designs
- Enclosure Designs
  
## Circuit Design

The schematic mainly consists of four main parts:

- **Adder Circuit**
- **Subtractor Circuit**
- **Multiplier Circuit**
- **Gain and DC Shift Adjustment**
- **Power Supply**

We selected the TL072 op-amp for the implementation of the above circuits due to its key characteristics that align well with our requirements. Below are the key reasons for this choice:

- *High Slew Rate:* The TL072 features a high slew rate of approximately 13 V/µs, allowing it to handle fast signal transitions accurately without distortion, which is crucial for our circuit implementations.
- *Low Noise:* It has low total harmonic distortion (THD) and minimal noise, helping to maintain signal integrity and ensure clean output in our designs.
- *Low Offset Voltage:* The op-amp offers a low input offset voltage, reducing errors and enhancing precision in signal amplification, which is essential for accurate circuit performance.

### Adder Circuit

The adder circuit combines two input signals using operational amplifiers (op-amps). It features a summing amplifier to add the signals and an inverting amplifier to adjust the output’s polarity and gain. The summing amplifier produces a weighted sum of the inputs, while the inverting amplifier refines the signal, allowing for precise control over the final output.

<p align="center">
  <img src="https://github.com/user-attachments/assets/9e944806-271d-4481-b9cb-2fa1dc64b246" alt="Adder" width="600"/>
</p>

### Subtractor Circuit

The subtractor circuit is designed by first inverting one of the input signals using an inverting amplifier. The inverted signal is then combined with the other signal through a summing amplifier. This setup effectively subtracts the inverted signal from the original signal, performing the desired subtraction operation. The use of operational amplifiers in this configuration ensures accurate and reliable signal subtraction.

<p align="center">
  <img src="https://github.com/user-attachments/assets/3bea2f84-4499-440b-9041-86f808dd073d" alt="Adder" width="600"/>
</p>

### Multiplier Circuit

Initially, we tested a logarithmic method for creating a multiplier circuit. Although the theoretical concept behind this approach was sound, it did not provide the expected practical results.

To overcome this, we implemented an alternative circuit design using two summing amplifiers and a differential amplifier. In this configuration, the first summing amplifier adds the two input signals \(Vx\) and \(Vy\) and provides an inverted sum. The output from this amplifier is then fed into a second summing amplifier along with twice one of the input signals, resulting in the difference between the input signals. After obtaining both the sum and the difference of the signals, these outputs are squared separately. Finally, a differential amplifier calculates the difference between the squared outputs, resulting in the expression \(Vx + Vy)^2 - (Vx - Vy)^2 = 4VxVy, which provides the desired multiplication of the input signals.

<p align="center">
  <img src="https://github.com/user-attachments/assets/24d5f9cd-76cf-4813-b381-2cc11cbb1ed1" alt="Adder" width="600"/>
</p>

### Gain and DC Shift Adjustment
<p align="center">
  <img src="https://github.com/user-attachments/assets/4e128993-1ed5-4153-86eb-dc8d122371be" alt="DC" width="45%" />
  <img src="https://github.com/user-attachments/assets/e246b901-ba9e-4014-b847-f5cd2cc5259f" alt="Gain" width="45%" />
</p>


### Power Supply

![Power](https://github.com/user-attachments/assets/58f3a752-d28f-4143-83af-10abea5d1ecb)
