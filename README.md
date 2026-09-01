# Smart Modular Workstation for Disaster Relief

**🏆 Runner-Up — Vyoma Design-a-thon (Problem Statement 4)**

An air-deployable, modular field station designed to provide power, communication, medical support, and survival resources within minutes of a natural disaster striking a remote or infrastructure-damaged region.

![Final Assembly](IMAGES/CAD_image_2.png)

*Full system with parachute deployed during descent phase*

---

## Overview

Floods, earthquakes, and other large-scale disasters routinely knock out local power, communication, and medical infrastructure right when they're needed most. This project designs a **75 kg air-droppable workstation** that can be delivered by helicopter or large drone and made fully operational within minutes of touchdown — no ground infrastructure required.

The system is split into four independent modules, each self-contained and field-serviceable:

| Module | Function |
|---|---|
| **1. Power & Communication** | LiPo battery bank, solar array, Raspberry Pi IoT dashboard, ham radio, satellite GPS |
| **2. Medical & Sustenance** | First-aid supplies, dehydrated food, compact water purification |
| **3. Survival Kit** | Tools, rope, fire starters, flare gun, thermal imaging camera |
| **4. Deployment Mechanism** | Parachute + airbag descent system engineered for a safe touchdown at up to 20 m/s |

---
## Individual Contribution
 
This section clarifies individual scope within a 4-person design-a-thon team. Scope covered:
 
| Area | Scope |
|---|---|
| 📐 **CAD Modeling** | Complete system CAD across all four modules — power/comms enclosure, medical/survival module, structural frame, and deployment mechanism housing |
| 💡 **Design Thinking** | Concept ideation and problem framing for the design-a-thon brief, including defining the modular (independently serviceable) architecture |
| 🏗️ **Structural Analysis (FEA)** | Static structural FEA for worst-case corner-impact load cases (30,000 N design load), computing deformation and Factor of Safety across one-, two-, and four-corner impact scenarios |
 
Descent/impact-velocity CFD and the power/communication electronics were handled by other team members.
 
### Skills Learnt
 
![CAD](https://img.shields.io/badge/-Complex%20Assembly%20CAD-455A64?style=flat&logoColor=white)
![FEA](https://img.shields.io/badge/-Static%20Structural%20FEA-1565C0?style=flat&logoColor=white)
![Design Thinking](https://img.shields.io/badge/-Design%20Thinking%20%2F%20Ideation-FF6F00?style=flat&logoColor=white)
![Cross-Team Coordination](https://img.shields.io/badge/-Cross--Team%20Coordination-6A1B9A?style=flat&logoColor=white)
 
- Modeling a multi-module system as independently serviceable assemblies, rather than one monolithic CAD structure
- Setting up worst-case structural load cases (single-, double-, and quad-corner impact) and interpreting Factor of Safety against a target design margin
- Concept-to-brief design thinking under a fixed competition problem statement and timeline
- Coordinating structural/CAD design decisions against inputs from teammates' descent-CFD and electronics work, so the frame and mounting points stayed consistent with the rest of the system

---

## Key Features

- **Modular architecture** — each unit can be transported, serviced, or reconfigured independently
- **Hybrid power system** — solar panels + manual hand-crank generator for energy redundancy
- **Real-time telemetry** — Raspberry Pi 5 IoT dashboard tracks power, GPS, and occupancy data
- **Engineered descent system** — parachute + CO₂ airbags reduce terminal velocity from ~31 m/s to ~6.2 m/s
- **Rugged operating range** — functions from −10°C to 40°C, resistant to water, dust, and debris

---

## Engineering Analysis

### Descent & Impact Calculations
The team calculated terminal velocity using standard drag equations, then validated it against CFD simulation:

- Without parachute: **~30.7 m/s**
- With parachute deployed: **~6.2 m/s** (analytical) — confirmed by CFD at **~6 m/s**

![CFD Descent Analysis](IMAGES/Parachute_sim.png)
*CFD velocity contour of the parachute-airbag descent phase*

### Structural Validation (FEA)
Static structural simulations were run for worst-case corner-impact scenarios at a design load of 30,000 N (vs. an actual estimated impact force of 7,500 N), giving a **Factor of Safety of 4.0**.

| Impact Case | Max Deformation | Result |
|---|---|---|
| One corner | 0.80 mm | ![One corner](IMAGES/strees_sim.png) |
| Two corners | 1.83 mm | ![Two corners](IMAGES/Deform2.png) |
| All four corners | 1.0 mm | ![All corners](IMAGES/deform3.png) |

---

## Internal Layout

![Internal Module Layout](IMAGES/CAD_image.png)
*Cutaway view showing the internal arrangement of survival kit, power system, and structural components*

---

## Mission Use Case

In the aftermath of a disaster, the workstation is air-dropped from ~1000 m altitude. Onboard GPS/IMU sensors guide it to the drop zone during descent; the parachute and airbag system bring it down safely. On landing, solar panels deploy automatically, satellite/ham radio links establish communication, and the IoT dashboard comes online — turning the unit into a mobile command center for relief teams to coordinate search, medical response, and drone-based aerial assessment.

---

## Tools & Technologies

`SolidWorks` `ANSYS Fluent (CFD)` `Finite Element Analysis (FEA)`

---

## Team

Developed by **Akula Uday Kiran, Kiran V Airani, Shanthosh K V, and Tejas L** — Department of Aerospace Engineering, RV College of Engineering.

Submitted for the Vyoma Design-a-thon, Problem Statement 4 (May 2025).

---

## Recognition

![Award Ceremony](IMAGES/AWARDING.jpeg) *Team receiving the Runner-Up award at Vyoma Design-a-thon*
