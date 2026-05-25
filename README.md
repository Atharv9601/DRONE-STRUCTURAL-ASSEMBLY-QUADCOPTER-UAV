# Quadcopter UAV – Structural Assembly (CATIA V5) 🚁🧩

Modular quadcopter frame designed for lab testing and rapid prototyping, focusing on lightweight structure, replaceable arms, and clean integration of electronics (FC, ESCs, LiPo, GPS, companion computer).

---

## 1. Project Overview 📌

This project contains the mechanical design of a quadcopter UAV structural assembly developed in **CATIA V5** (Part Design & Assembly Design).  
The frame is optimized for **FDM 3D printing** and basic machining, with attention to stiffness, vibration behaviour, and fast assembly in a lab environment.

Key goals:

- Support four brushless motors with appropriate propeller clearance.  
- Provide a central bay for **flight controller, ESCs, LiPo battery, GPS, and wiring**.  
- Enable **modular arms** for easy replacement and configuration changes.

---

## 2. System Architecture 🧱

The structural assembly is split into functional modules to simplify design, analysis, and manufacturing.

### 2.1 Central Frame / Payload Enclosure 🎛️

- Houses flight controller, 4‑in‑1 ESC or individual ESCs, LiPo battery, GPS and wiring.  
- Includes mounting bosses, ventilation cut‑outs, and **cable routing channels** to separate power and signal paths.  
- Designed with parametric wall thickness and rib patterns to balance stiffness and print time.

### 2.2 Motor Arms 🔩

- Four arms extending radially at 90° from the centre.  
- Cross‑section geometry tuned for **bending stiffness** and reduced weight using ribs and fillets.  
- Parametric length and section allow quick adaptation to different propeller diameters or motor sizes.

### 2.3 Motor Mounts ⚙️

- End‑plates at each arm tip with standardized bolt patterns for typical brushless motors.  
- Propeller disk envelopes checked to avoid interference with the frame and adjacent props.  
- Local reinforcement around mounting holes to handle motor torque and landing impacts.

### 2.4 Landing Elements 🛬

- Simple skids or landing pads mounted to the central frame.  
- Designed to protect the payload and propellers on touchdown.  
- Geometry compatible with FDM printing (no excessive overhangs, stable contact surfaces).

### 2.5 Fasteners & Interfaces 🧷

- Arms bolted to the central frame via **standardized boss and bolt patterns**.  
- Single fastener size used wherever possible to simplify assembly and maintenance.  
- Interfaces designed for repeatable positioning and easy replacement of individual arms.

---

## 3. Design Objectives 🎯

- **Modularity**  
  Arms and landing elements are detachable, supporting quick repair and configuration changes without modifying the core frame.

- **DFMA for FDM 3D Printing** 🧪  
  Wall thickness, fillet radii, and rib layout optimized for typical FDM printers, reducing print time and ensuring sufficient stiffness under vibration loads.

- **Component‑Aware Layout** 🧠  
  Installation zones reserved for FC/ESC, LiPo, GPS, and companion computer (e.g. Raspberry Pi), with attention to CG location and EMI separation between power and signal wiring.

- **Portfolio‑ready Documentation** 📄  
  Complete 3D assemblies, 2D drawings, and BOM prepared for use in CVs, portfolios, and technical interviews.

---

## 4. CAD Workflow 🧩

### 4.1 Envelope & Layout Definition 📐

- Set overall diagonal size based on target **propeller diameter** and desired payload volume.  
- Fix motor positions and arm angles (90° X configuration) around the centre of gravity.  
- Define keep‑out zones for propeller disks and electronics.

### 4.2 Part Modelling (CATIA V5 – Part Design) 🧱

Modeled as separate parts:

- Central frame / payload enclosure  
- Motor arms  
- Motor mounts / end‑plates  
- Landing skids or pads  
- Fastener interfaces (bosses, spacers, brackets as needed)

Parametric features:

- Arm length and thickness  
- Wall thickness of the enclosure  
- Mounting hole positions and diameters  
- Rib spacing and height for stiffness tuning

### 4.3 Assembly Creation (CATIA V5 – Assembly Design) 🧷

- Insert individual parts and constrain using coincidence, offset, and angle constraints.  
- Align motors and props relative to the centre to maintain geometric balance.  
- Validate clearances for propellers, landing gear, and internal electronics.

### 4.4 Clearance & Interference Checks ✅

- Verify that propeller disks do not intersect the frame, arms, or each other.  
- Confirm sufficient space for LiPo, FC, ESCs, and wiring inside the enclosure.  
- Check that cable routing paths avoid sharp bends and potential chafing points.

### 4.5 Detailing & Documentation ✏️

- Create **2D drawings** for all structural parts with complete dimensioning and GD&T where relevant.  
- Prepare an **exploded view** and **ballooned BOM** of the full assembly.  
- Export views and drawings as images/PDFs for portfolio and presentation use.

---

## 5. Key Features 🌟

- **Modular Arm Design**  
  - Bolt‑on arms with standardized interfaces.  
  - Easy arm replacement and length scaling driven from a single parameter set.

- **Lightweight yet Manufacturable** 🧵  
  - Simple cross‑sections, ribs, and fillets compatible with common FDM printers.  
  - Geometry avoids unnecessary support material and minimizes print failures.

- **Component‑Aware Geometry** 🔌  
  - Mounting patterns and internal standoffs sized from real component data (motors, FC, ESC, LiPo).  
  - Clear separation between high‑current power paths and sensitive signal wiring.

- **Documentation for Engineering Use** 📚  
  - Clean assemblies and drawings suitable for code reviews, design discussions, and job applications.  
  - Highlights multi‑body assembly design, structural thinking, and DFMA knowledge.

---

## 6. Possible Extensions 🚀

- Add a detailed **battery mounting and quick‑release mechanism** in the central bay.  
- Introduce **foldable or detachable arms** using hinges or quick‑release joints driven by the same parametric model.  
- Integrate simplified motor and propeller models for visualization and basic mass distribution checks.  
- Generate rendered views for slides and portfolio (e.g. CATIA rendering or export to Fusion 360/KeyShot).

---

## 7. Repository Structure 📂

```text
.
├── /CAD/
│   ├── Central_Frame.CATPart
│   ├── Motor_Arm.CATPart
│   ├── Motor_Mount.CATPart
│   ├── Landing_Skid.CATPart
│   └── Quadcopter_Assembly.CATProduct
├── /Drawings/
│   ├── Central_Frame_Drawing.CATDrawing
│   ├── Motor_Arm_Drawing.CATDrawing
│   ├── Motor_Mount_Drawing.CATDrawing
│   └── Assembly_Exploded_BOM.CATDrawing
```

*(File names and folders are suggestions – adapt them to your actual structure.)*

---

## 8. Tools & Technologies 🧰

- **CAD:** CATIA V5 (Part Design, Assembly Design)  
- **Manufacturing target:** FDM 3D printing (PLA / PETG) and basic machining  
- **Domain:** UAV / drone mechanical design, structural layout, and DFMA
