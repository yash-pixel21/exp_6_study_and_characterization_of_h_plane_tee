# exp_6_study_and_characterization_of_h_plane_tee

# Experiment 6 — Study and Characterization of H-Plane Tee

---

## Aim

To study and measure the characteristics of an H-plane tee.

## Apparatus Used

Klystron power supply, klystron mount with tube, isolator, variable attenuator, frequency meter, slotted line section, H-plane tee, detector mount / crystal detector, matched terminations, VSWR meter, waveguide stands.

## Experimental Setup

<img width="746" height="446" alt="image" src="https://github.com/user-attachments/assets/5cc5ccb7-2004-4a24-8e14-044ebcef6cad" />

---

## Theory

In an H-plane tee an auxiliary waveguide arm is fastened perpendicular to the **narrow wall** of the main guide. It is a three-port device in which the axis of the auxiliary (side) arm is parallel to the planes of the magnetic field of the main guide, and the coupling from the main guide to the branch guide is by means of **magnetic fields** — hence the name H-plane tee.

The perpendicular arm is generally taken as the input and the other two arms are in **shunt** with it, so the junction is also called a **shunt tee**.

Because of the symmetry of the tee, when power enters the auxiliary arm and the two main arms 1 and 2 are terminated in identical loads, the power supplied to each load is **equal and in phase**. Conversely, if two signals of equal amplitude and the same phase are fed into the two main arms, they add together in the side arm. The H-plane tee therefore acts as an **adder**.

### Summary of behaviour

| Feed point | Result |
|---|---|
| Auxiliary (H) arm | Equal split into arms 1 and 2, in phase |
| Arms 1 and 2 (equal, in phase) | Signals add at the H-arm |
| Function | Adder, shunt tee |

---

## Procedure

1. Set up the microwave bench: klystron power supply → klystron mount → isolator → variable attenuator → frequency meter → slotted section → component under test (H-plane tee) → detector mount → VSWR meter.
2. Keep the control knobs of the klystron power supply at their initial settings (mode switch: AM; beam voltage knob: fully anti-clockwise; repeller voltage knob: fully clockwise; meter switch: beam current) and switch on the supply, the VSWR meter and the cooling fan.
3. Energise the klystron for maximum output at the desired frequency by adjusting the beam and repeller voltages; measure the operating frequency with the frequency meter and then detune it.
4. **Reference reading:** without the H-plane tee in the line, set the variable attenuator to obtain a convenient full-scale reference reading on the VSWR meter. Note the attenuator setting **A₁** dB.
5. **Insert the component:** connect the H-plane tee in the line, feeding the arm under test and terminating the remaining arms in matched loads.
6. Reduce the attenuation until the VSWR meter reads the same reference value. Note the attenuator setting **A₂** dB. The difference (A₁ − A₂) dB gives the coupling/isolation for that pair of ports.
7. **Power division:** feed the H-arm, terminate one collinear arm in a matched load and measure the power at the other collinear arm; repeat with the arms interchanged. The measured coupling should be about **3 dB** for each collinear arm.
8. **Isolation:** feed the H-arm and measure the power coupled to the isolated port, with all other ports match-terminated.
9. **VSWR of each port:** feed the port under test, terminate the remaining ports in matched loads, and measure the VSWR using the slotted line.
10. Repeat the measurements for each of the three ports.

---

## Observation

### Observations

**Operating Parameters:**
* Resonant Frequency: `9.45 GHz`
* Signal Source: Reflex Klystron (1 kHz Square-Wave Modulated)
* Reference Attenuator Setting ($A_1$): `38.0 dB` (Direct connection without H-Plane Tee)

#### Table 1: Power Division & Coupling Characteristics (Input at H-Arm, Port 3)
| Input Port | Output Port | Terminated Port | Attenuator Reading $A_2$ (dB) | Power Received $P_{\text{out}}$ (dB) | Coupling Factor $(A_1 - A_2)$ (dB) | Theoretical Value (dB) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Port 3 (H-arm)** | Port 1 (Collinear 1) | Port 2 (Matched Load) | 34.9 | -3.1 | 3.1 | 3.0 |
| **Port 3 (H-arm)** | Port 2 (Collinear 2) | Port 1 (Matched Load) | 34.8 | -3.2 | 3.2 | 3.0 |

#### Table 2: Transmission and Cross-Coupling Measurements
| Input Port | Output Port | Terminated Port | Attenuator Reading $A_2$ (dB) | Power Received $P_{\text{out}}$ (dB) | Coupling / Loss $(A_1 - A_2)$ (dB) |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **Port 1** | Port 2 | Port 3 (Matched Load) | 35.8 | -2.2 | 2.2 |
| **Port 1** | Port 3 (H-arm) | Port 2 (Matched Load) | 34.9 | -3.1 | 3.1 |
| **Port 2** | Port 3 (H-arm) | Port 1 (Matched Load) | 34.8 | -3.2 | 3.2 |

#### Table 3: Port VSWR Measurements
| Port Under Test | Terminated Ports | $V_{\max}$ (V) | $V_{\min}$ (V) | Measured VSWR ($S = V_{\max} / V_{\min}$) |
| :---: | :---: | :---: | :---: | :---: |
| **Port 1 (Collinear Arm 1)** | Ports 2 & 3 (Matched Loads) | 1.45 | 1.00 | 1.45 |
| **Port 2 (Collinear Arm 2)** | Ports 1 & 3 (Matched Loads) | 1.43 | 1.00 | 1.43 |
| **Port 3 (H-Plane Arm)** | Ports 1 & 2 (Matched Loads) | 1.82 | 1.00 | 1.82 |

---

### Calculations

**1. Power Division Difference ($\Delta P$):**
$$\Delta P = \vert{}P_{\text{Port 1}} - P_{\text{Port 2}}\vert{} = \vert{}-3.1\text{ dB} - (-3.2\text{ dB})\vert{} = 0.1\text{ dB}$$
*(Confirms nearly equal 3 dB power division between both collinear arms)*

**2. Experimental Scattering Matrix ($[S]$):**
$$[S] = \begin{bmatrix}  0.18 & 0.77 & 0.70 \\  0.77 & 0.17 & 0.69 \\  0.70 & 0.69 & 0.29  \end{bmatrix}$$

---

### Inferences

1. When microwave power enters the **H-plane arm (Port 3)**, it splits almost equally between **Port 1** ($3.1\text{ dB}$) and **Port 2** ($3.2\text{ dB}$) with identical phase ($0^\circ$), validating the adder/shunt tee property.
2. The measured VSWR values for the collinear arms are approximately **1.44**, while the auxiliary H-arm gives **1.82**, matching the expected slight mismatch at the junction without internal tuning elements.

## Precautions

* Check all connections before switching on the kit.
* Keep all knobs at minimum before switching on the power supplies; the HT must be OFF while switching on the mains.
* Do not exceed a beam current of 30 mA, and keep the repeller voltage within the specified range.
* Terminate all unused ports in matched loads while taking readings.
* Do not look directly into an open waveguide.

## Result

The characteristics of the H-plane tee were studied.
