# OpenSensorDAQ:
A Fast High resolution platform for analog sensing, Analog to Digital conversion and Data acquisition with low noise characteristics and USB interfacing with the PC.

Visit here for full Micropipette-Aspiration-Setup: https://github.com/harshjn/MicroPipette-Aspiration-Setup

Cite this project as:
```bibtex
@misc{jain2025opensensordaq,
  author       = {Jain, Harsh},
  title        = {{OpenSensorDAQ}: Fast High-Resolution and Low-cost Analog Sensor
                  Data Acquisition System},
  year         = {2025},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/harshjn/OpenSensorDAQ}}
  }
```
1. **Sensor**: 0.2MPa pressure sensor, https://robu.in/product/pro-range-pr12-p145b-pressure-sensors-00-2mpa-0-54-5v-g1-4
2. **Analog-Digital DAQ**: National Instruments USB-6002, https://www.digikey.in/en/products/detail/ni/782602-01/12817647
3.**Amplifier Design**: Based on AD624, https://github.com/harshjn/OpenSensorDAQ/blob/main/Amplifier%20Gain%20Circuit%20diagram.jpg

Electronic transducers typically utilize Wheatstone bridge configurations serve that serve as the foundation for numerous sensing methodologies, including strain gauges, pressure transducers, and load cells. These impedance-based sensors operate on the principle of resistance variation converted to measurable voltage differentials.

The bridge circuit receives excitation from a precision reference voltage source, with the resulting signal captured via single-ended or differential input configurations by an Analog-to-Digital Converter (ADC) within the Data Acquisition (DAQ) system architecture.

For applications requiring enhanced signal integrity from low-amplitude sensor outputs, two critical performance parameters become essential:

1. **High SNR (Signal-to-Noise Ratio)** achieved through minimized noise floor characteristics
2. **Enhanced bit depth resolution** of the analog-to-digital conversion process

Implementing high-frequency sampling rates (≥1 kHz) provides a significant advantage through the application of signal averaging techniques. When the measured physical phenomenon exhibits bandwidth characteristics substantially lower than the Nyquist frequency of the acquisition system, oversampling followed by digital averaging effectively reduces uncorrelated noise by a factor proportional to √n, where n represents the number of averaged samples.

This oversampling methodology enables effective noise averaging while maintaining good accuracy of measurement for the underlying physical process being measured.

In OpenSensorDAQ, we put the bias voltage and voltage measurement via the same circuit board, so as to remove fluctuations in the bias voltage by design. 

Future plan:
1. **Can be powered by 12-24 V DC**
2. **ADS8866 provides high 16-bit resolution and sampling rate of 100k Hz.**
3. A low pass filter removes high frequency noise. 
4. Circuit to be designed in open-source KiCad. The circuit diagrams are printed and the components soldered on the board. Electically shielded box is usually preferred.
5. MicroController circuit interfaced to the ADC circuit and communicating with PC via Direct SPI/I2C to USB bridge over USB Type-C. 
