# OpenSensorDAQ:
A Fast High resolution (16-bit) analog sensor Analog to Digital conversion and Data acquisition system with low noise characteristics, built in microprocessor for serial communication and modular design for interfacing. 

Electronic transducers utilizing Wheatstone bridge configurations serve as the foundation for numerous sensing methodologies, including strain gauges, pressure transducers, and load cells. These impedance-based sensors operate on the principle of resistance variation converted to measurable voltage differentials.

The bridge circuit receives excitation from a precision reference voltage source, with the resulting signal captured via single-ended or differential input configurations by an Analog-to-Digital Converter (ADC) within the Data Acquisition (DAQ) system architecture.

For applications requiring enhanced signal integrity from low-amplitude sensor outputs, two critical performance parameters become essential:

1. **High SNR (Signal-to-Noise Ratio)** achieved through minimized noise floor characteristics
2. **Enhanced bit depth resolution** of the analog-to-digital conversion process

Implementing high-frequency sampling rates (≥1 kHz) provides a significant advantage through the application of signal averaging techniques. When the measured physical phenomenon exhibits bandwidth characteristics substantially lower than the Nyquist frequency of the acquisition system, oversampling followed by digital averaging effectively reduces uncorrelated noise by a factor proportional to √n, where n represents the number of averaged samples.

This oversampling methodology enables effective noise averaging while maintaining good accuracy of measurement for the underlying physical process being measured.

In OpenSensorDAQ, we put the bias voltage and voltage measurement via the same circuit board, so as to remove fluctuations in the bias voltage by design. 
A low pass filter removes high frequency noise. 

The circuit diagrams are printed and the components soldered on the board. Electically shielded box is usually preferred. 
