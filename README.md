# Programmable ADC IP for Mixed-Signal SoC Integration

A high-performance, configurable Analog-to-Digital Converter (ADC) IP core designed for mixed-signal SoC applications. This project combines analog front-end design, SystemVerilog RTL, mixed-signal verification, and ASIC-oriented design flows to demonstrate a complete ADC subsystem suitable for modern embedded and data acquisition systems.

---

# Overview

I implemented a programmable SAR-based ADC architecture capable of converting real-world analog signals into digital data for processing within a System-on-Chip (SoC).

The design integrates:
- Analog signal conditioning
- SAR conversion logic
- Digital configuration/control
- Verification infrastructure
- ASIC-oriented design and layout flows

The goal of this project is to bridge analog and digital hardware domains while exploring complete mixed-signal IP development workflows.

---

# Key Features

## ADC Capabilities
- Configurable ADC resolution:
  - 12-bit
  - 14-bit
  - 16-bit
- Programmable sampling rate:
  - 1–5 MSPS
- SAR (Successive Approximation Register) ADC architecture
- Real-time performance monitoring
- Built-in calibration support

## Analog Front-End
- Programmable Gain Amplifier (PGA)
  - Gain settings: 1x, 2x, 3x, 4x
- Sample-and-Hold Circuit
- High-speed Comparator
- SAR DAC Array

## Digital Features
- APB Slave Interface
- SystemVerilog RTL implementation
- Modular architecture
- Configurable control registers
- Integrated monitoring and status logic

---

# Architecture

The ADC is implemented using a mixed-signal architecture that combines analog conversion blocks with digital control logic.

## Analog Blocks
- Sample & Hold
- Comparator
- Programmable Gain Amplifier (PGA)
- DAC Array

## Digital Blocks
- SAR Controller
- APB Interface
- Control Unit
- Monitoring Logic

---

# SAR ADC Working Principle

The ADC operates using the Successive Approximation Register (SAR) method:

1. The analog signal is sampled and held.
2. The SAR controller generates a trial digital value.
3. The DAC converts this value into an analog reference.
4. The comparator compares:
   - Input voltage (Vin)
   - DAC reference voltage (Vdac)
5. The SAR logic updates bits iteratively until the closest digital approximation is achieved.

This enables efficient and accurate analog-to-digital conversion with low power consumption.

---

# Supported Toolchains

## Commercial EDA Flow
- Cadence Virtuoso
- Spectre
- AMS Designer
- Calibre
- IC Compiler
- Questa
- VCS

## Open-Source Flow
- Sky130 PDK
- Xschem
- Magic
- ngspice
- Netgen
- OpenLane
- Verilator

---

# Verification Infrastructure

The project includes comprehensive verification support:

- UVM-compliant testbenches
- Functional verification
- Coverage-driven verification
- Mixed-signal simulation
- Corner-case testing
- Automated regression infrastructure

---

# Project Structure

```text
programmable-adc/
├── rtl/                    # SystemVerilog RTL implementation
├── analog/                 # Analog schematic/layout files
├── tb/                     # Verification environment
├── simulation/             # Simulation configurations/results
├── layout/                 # DRC/LVS verification
├── flow/                   # ASIC design flows
├── scripts/                # Automation scripts
├── integration/            # SoC integration examples
├── docs/                   # Documentation
└── vyges-metadata.json     # Vyges metadata
```

---

# RTL Modules

## Core Modules
- `programmable_adc.sv`
- `programmable_adc_sar_controller.sv`
- `programmable_adc_dac_array.sv`
- `programmable_adc_comparator.sv`
- `programmable_adc_sample_hold.sv`
- `programmable_adc_pga_stage.sv`
- `programmable_adc_apb_interface.sv`

---


# Verification Goals

The verification environment validates:

- ADC functional correctness
- Resolution configurability
- Sampling-rate behavior
- Calibration functionality
- Corner conditions
- Timing behavior
- APB register configuration
- Mixed-signal interactions

---

# ASIC-Oriented Design Flow

The project demonstrates:
- RTL design
- Mixed-signal integration
- Analog schematic entry
- SPICE simulation
- Layout generation
- DRC/LVS verification
- Synthesis flow integration

---

# Applications

This ADC IP can be integrated into:

- IoT sensor systems
- Embedded SoCs
- Audio acquisition systems
- Industrial monitoring
- Biomedical instrumentation
- High-speed data acquisition platforms

---

# Future Improvements

- Pipeline ADC architecture
- Power optimization
- Noise analysis
- Clock-domain synchronization
- Enhanced calibration engine
- DMA integration
- AXI interface support
- On-chip buffering
- Advanced verification coverage

---

# Learning Outcomes

This project explores:
- Mixed-signal IC design
- ADC architecture
- RTL design using SystemVerilog
- SoC integration
- Verification methodologies
- Analog-digital interfacing
- ASIC design workflows
- EDA tooling ecosystems

---
