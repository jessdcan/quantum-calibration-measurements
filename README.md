# Quantum Calibration Measurements

This repository contains experimental work and analysis for quantum qubit calibration using Qiskit Pulse, focusing on various quantum characterization techniques including frequency sweeps, Rabi oscillations, Ramsey measurements, and T1/T2 relaxation times. The experiments specifically investigate how decoherence occurs in qubit performance over time.

## 📚 Project Overview

This repository documents a comprehensive study of quantum qubit calibration techniques as part of ELEN4022 Lab 3 (2022). The work involves practical implementation of quantum characterization protocols using IBM Quantum hardware through Qiskit Pulse framework.

## 🏗️ Repository Structure

```
quantum-calibration-measurements/
├── calibration_lab.ipynb                    # Main Jupyter notebook with calibration experiments
├── QC Lab 3.bib                  # Bibliography and references
├── Calibration and Pulse Control in Quantum Machine.pdf  # Supporting documentation
├── Brisbane high decoherence/    # Experimental results with high decoherence rates
│   ├── dynamic decoupling.png
│   ├── freq_2.png
│   ├── freq.png
│   ├── hanecho.png
│   ├── rabi.png
│   ├── ramsey.png
│   └── t1.png
├── Brisbane low decoherence/     # Experimental results with low decoherence rates
│   ├── freq.jpg
│   ├── hancho.jpg
│   ├── ramsey.jpg
│   ├── sigAmp.jpg
│   └── t1.jpg
└── submission/                   # Academic submission materials
    └── ELEN4022_LAB3_2022_Dworcan_Jess/
```

## 🔬 Experimental Techniques

The repository covers several key quantum calibration methods:

### Understanding Decoherence
Decoherence is the loss of quantum coherence due to interaction with the environment. In quantum computing, it manifests as:
- **T1 (Energy Relaxation)**: Energy loss from excited to ground state
- **T2 (Dephasing)**: Loss of phase information in quantum superpositions

The experiments compare measurements under different decoherence conditions to understand their impact on calibration accuracy.

### Quantum Characterization Methods

### 1. **Frequency Sweep**
- Qubit frequency determination using spectroscopy
- Bandwidth analysis around estimated frequencies
- Frequency step optimization

### 2. **Rabi Oscillations**
- Amplitude calibration for π/2 and π pulses
- Pulse duration optimization
- Signal amplitude analysis

### 3. **Ramsey Measurements**
- T2* coherence time determination
- Frequency detuning analysis
- Echo sequence implementation

### 4. **Relaxation Measurements**
- T1 relaxation time characterization
- T2 echo measurements
- Dynamic decoupling experiments

## 🛠️ Technical Implementation

### Dependencies
- **Qiskit**: Quantum computing framework
- **Qiskit Runtime**: IBM Quantum runtime service
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization

### Hardware Configuration
- **Backend**: IBM Quantum hardware (least busy operational backend)
- **Sampling Time**: 0.5 ns
- **Timing Constraints**: 
  - Acquire alignment: 8 samples
  - Pulse alignment: 8 samples
  - Granularity: 8 samples

### Key Parameters
- **Frequency Sweep**: 40 MHz bandwidth, 1 MHz steps
- **Pulse Duration**: Optimized for π/2 and π rotations
- **Measurement Integration**: Backend-default integration times

## 📊 Results

The repository contains two sets of experimental results demonstrating different decoherence characteristics:

### Brisbane Low Decoherence

- Successful frequency measurements with minimal noise
- Optimized Rabi oscillations showing clear sinusoidal behavior
- Clear Ramsey fringes with good visibility
- Reliable T1 measurements with exponential decay fitting
- Signal amplitude characterizations with high signal-to-noise ratio

### Brisbane High Decoherence

- Frequency sweep artifacts due to environmental noise
- Suboptimal pulse calibrations affected by decoherence
- Ramsey measurement noise reducing fringe visibility
- T1 measurement challenges with non-exponential decay
- Dynamic decoupling issues from rapid dephasing

## 🚀 Getting Started

### Prerequisites

1. Install Python 3.7+
2. Install required packages:

   ```bash
   pip install qiskit qiskit-ibm-runtime numpy matplotlib jupyter
   ```

### Running Experiments

1. Clone this repository
2. Open `calibration_lab.ipynb` in Jupyter Notebook
3. Ensure you have IBM Quantum account credentials
4. Run cells sequentially to perform calibrations

### IBM Quantum Access

- Sign up at [IBM Quantum Experience](https://quantum-computing.ibm.com/)
- Generate API token
- Configure Qiskit Runtime service

## 📖 Academic Context

This work was completed as part of **ELEN4022 Lab 3 (2022)** under the supervision of academic staff. The experiments demonstrate practical application of quantum characterization techniques taught in quantum computing courses.

## 🔍 Key Findings

- **Frequency Calibration**: Successfully determined qubit frequencies with MHz precision under varying decoherence conditions
- **Pulse Optimization**: Achieved reliable π/2 and π pulse calibrations, with performance degradation observed in high decoherence environments
- **Coherence Characterization**: Measured T1 and T2* times for qubit characterization, revealing the impact of environmental noise on measurement accuracy
- **Decoherence Analysis**: Demonstrated how different decoherence rates affect the quality of quantum measurements and calibration procedures
- **Error Analysis**: Identified common pitfalls in quantum calibration procedures and their relationship to environmental noise levels
