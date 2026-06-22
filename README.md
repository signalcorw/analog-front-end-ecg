# Analog Front-End ECG

Precision ECG signal acquisition chain using the
INA333 instrumentation amplifier
and ADS1115 16-bit ADC.

## Objective

Design and simulate a low-noise ECG analog front-end capable of:

- Amplifying ECG signals (0.5 mV – 5 mV)
- Rejecting common-mode interference (50 Hz mains noise)
- Filtering unwanted frequencies
- Providing a signal suitable for ADC conversion

---

## System Architecture

ECG Electrodes
→ INA333 Instrumentation Amplifier
→ High-Pass Filter (0.5 Hz)
→ Low-Pass Filter (150 Hz)
→ ADS1115 ADC
→ Digital Processing

---

## Current Status

### Completed

- [x] LTspice setup
- [x] Three-op-amp INA333 architecture implemented
- [x] Gain verification (G = 11)
- [x] Common-mode rejection test
- [x] Output offset verification
- [x] AC sweep / Bode analysis

### In Progress

- [ ] Real INA333 SPICE model integration
- [ ] ECG filter design
- [ ] ADS1115 interface modelling

### Planned

- [ ] Complete signal-chain simulation
- [ ] KiCad schematic capture
- [ ] PCB layout
- [ ] Hardware validation

---

## Simulation Results

| Test | Requirement | Result | Status |
|--------|--------|--------|--------|
| Gain (Rg = 10kΩ) | 11 ± 0.5 | 11.0 | PASS |
| Output Centre Voltage | 1.65 ± 0.05 V | 1.65 V | PASS |
| CMRR Test | Common-mode rejection | PASS | PASS |
| Flat-band Gain | 20.8 dB | 20.8 dB | PASS |

---

## Tools

- LTspice
- KiCad
- Python
- Arduino IDE

---

