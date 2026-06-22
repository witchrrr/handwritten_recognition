# Hardware Implementation of a Neural Network for Handwritten Digit Recognition on FPGA

## Overview

This project implements a fully connected neural network for handwritten digit recognition on an FPGA platform using SystemVerilog. The design processes 28×28 grayscale images and classifies digits from 0–9 using quantized neural network weights.

The architecture consists of:

* Average Pooling Layer (28×28 → 14×14)
* Hidden Dense Layer (32 neurons)
* Output Dense Layer (10 neurons)
* ReLU Activation Functions
* Maximum Selection Module (Digit Prediction)

The project was developed and simulated using Xilinx Vivado and targeted for FPGA deployment on the Pynq-Z2 platform.

---

## Features

* SystemVerilog-based neural network implementation
* 8-bit quantized weights and biases
* Modular hardware architecture
* End-to-end handwritten digit recognition pipeline
* Comprehensive testbenches for verification
* AXI4-Lite IP integration for FPGA deployment
* MNIST digit classification

---

## Architecture

Input Image (28×28)

↓

Average Pooling Layer

↓

Dense Layer 1 (32 Neurons + ReLU)

↓

Dense Layer 2 (10 Neurons)

↓

Maximum Selection (ArgMax)

↓

Predicted Digit

---

## Project Structure

```text
├── avg_pooling/
├── dense_layer_1/
├── dense_layer_2/
├── neuron/
├── relu/
├── select_max/
├── neural_network_top/
├── testbenches/
├── vivado_project/
├── python_model/
└── README.md
```

---

## Simulation Results

The design was validated through simulation using MNIST test images.

### Results

* Correct classification of handwritten digits
* Successful verification of all modules
* Functional end-to-end neural network pipeline
* 100% accuracy on tested simulation samples

---

## FPGA Implementation

The neural network was packaged as a custom AXI4-Lite IP and integrated into a Pynq-Z2 block design.

### Implementation Steps

1. Create custom neural network IP.
2. Package IP with AXI4-Lite interface.
3. Integrate into Vivado block design.
4. Generate bitstream and export hardware.
5. Control the design through Python/Jupyter on Pynq.

---

## Tools Used

* SystemVerilog
* Xilinx Vivado
* Pynq-Z2 FPGA Board
* Python
* Jupyter Notebook
* MNIST Dataset

---

## Future Improvements

* CNN-based architecture
* Full MNIST dataset validation
* Resource optimization
* Improved FPGA-software integration
* Higher classification accuracy

---

## Author

Pratyush Kumar

M.Tech VLSI Design

VIT Vellore

---

## License

This project is intended for educational and research purposes.
