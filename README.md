
# Manual Clinical Centrifuge

An electricity-independent, low-cost, and robust manual centrifuge designed for diagnostic testing (blood, urine, etc.) in rural and resource-limited healthcare settings.

This repository contains the documentation, CAD design insights, component lists, and manufacturing workflows for the project completed as part of the **TA212 (Manufacturing Processes)** course at **IIT Kanpur**.

---

## 📋 Table of Contents
- [Project Overview & Motivation](#-project-overview--motivation)
- [System Architecture & Working Principle](#-system-architecture--working-principle)
- [Technical Specifications & Components](#-technical-specifications--components)
- [Manufacturing Processes](#-manufacturing-processes)
- [Engineering Challenges & Troubleshooting](#-engineering-challenges--troubleshooting)
- [Key Advantages](#-key-advantages)
- [Future Scope](#-future-scope)
- [Project Team & Acknowledgments](#-project-team--acknowledgments)

---

## 💡 Project Overview & Motivation

### Context
Rural regions often suffer from unreliable electrical grids and lack essential medical infrastructure. Clinical centrifuges are vital diagnostic assets for performing basic blood and urine analyses, yet commercial models heavily rely on stable electrical power, feature high initial costs, and require frequent technical maintenance.

### Problem Statement
How can we build an affordable, robust, and mechanically driven diagnostic centrifuge capable of generating the high operational rotational speeds (RPM) necessary for fluid separation without relying on electrical power?

### Project Goal
To design, machine, and fabricate a completely manual, hand-cranked clinical centrifuge that is structurally stable, easy to maintain, modular, and highly affordable for rural clinics.

---

## ⚙️ System Architecture & Working Principle

The mechanical drivetrain converts slow, high-torque manual rotational input into high-speed, low-torque vertical spindle rotation through a structured, multi-stage transmission system:

1. **Manual Input:** A user rotates a rugged, single-handle hand crank.
2. **Spur Gear Transmission Multiplier:** The input drive runs through a compact assembly containing **4 sequential stages** of spur gear pairings. Each pairing features a $1:3$ gear ratio ($20\text{T}$ pinion driven by a $60\text{T}$ gear), yielding an overall speed amplification factor of:
   $$\text{Total Amplification} = 3 \times 3 \times 3 \times 3 = 3^4 = 81\times$$
   *(e.g., A gentle manual input of $60\text{ RPM}$ translates to a rapid output speed of $\approx 4,860\text{ RPM}$ at the final stage).*
3. **Axis Realignment:** A set of $1:1$ ratio bevel gears ($20\text{T}$) redirects horizontal shaft rotation into a vertical output axis.
4. **Centrifugal Separation:** The vertical spindle drives a custom main rotor fitted with 3D-printed mounts, smoothly spinning the diagnostic test tubes to induce rapid sedimentation.

---

## 🛠️ Technical Specifications & Components

| Component | Quantity | Description / Specifications |
| :--- | :---: | :--- |
| **Base Plate** | 1 | Heavy-duty foundational metal plate ensuring structural stabilization. |
| **L-Support / L-Plate** | 6 | Structural framing blocks providing rigid shaft/bearing mounting baselines. |
| **Spur Gears (20T & 60T)** | 4 each | $1.5\text{ Module}$ high-precision gears establishing the $81\times$ velocity boost. |
| **Bevel Gears (20T)** | 2 | $1.5\text{ Module}$ intersecting gears providing $90^\circ$ directional axis change. |
| **Handle Assembly** | 1 | Manual, robust hand crank optimized for ergonomic operation. |
| **Main Rotor Spindle** | 1 | Vertically oriented drive-shaft holding the centrifuge test-tube housing. |
| **Test Tube Holders** | 6 | Custom 3D-printed modular structural containment mounts. |
| **Axles & Bearings** | 6 | Ground shafts and matched rolling-element bearings to guide rotation. |

---

## 🏭 Manufacturing Processes

The manufacturing workflow integrated an end-to-end design-to-fabrication pipeline utilizing standard mechanical workshop procedures:

* **CAD Modeling & Assembly Simulation:** Parts were individually modeled, compiled, and checked for static/dynamic clearance constraints in CAD software.
* **Shearing, Cutting, & Drilling:** Metal stock plates were cut down to form the base foundation and structural L-plates before being precisely drilled for axle clearance holes.
* **Turning & Facing:** Rotational shafts and custom axles were machined down to design tolerances on traditional lathe machines.
* **Milling:** Used to machine precision slotted alignment channels in mounting hardware to permit fine positioning adjustments of gear meshes.
* **Gear Hobbing/Manufacturing:** $1.5\text{ Module}$ spur and bevel gears were machined to meet rigorous angular tracking requirements.
* **Additive Manufacturing:** Fused Deposition Modeling (FDM) 3D printing was deployed to quickly fabricate the specialized lightweight rotor mounts and test-tube holders.
* **Assembly & Calibration:** Manual alignment, component shimming, and dynamic testing runs were completed to verify separation performance before and after centrifugation.

---

## 🚀 Engineering Challenges & Troubleshooting

| Encountered Challenge | Root Cause | Engineering Solution Implemented |
| :--- | :--- | :--- |
| **Axle Misalignment** | Minor machining discrepancies across parallel L-frame plates. | Inserted matched precision metal washers to subtly raise and realign the L-plates. |
| **Gear Jamming / Binding** | Excessively tight dimensional tolerances along key mating shafts. | Opened up shaft clearance tolerances and polished matching contact zones. |
| **Severe High-RPM Vibrations** | Unbalanced rotational masses and lack of rigid structural damping. | Welded additional triangular gussets and mechanical braces at high-stress frame sections. |
| **Test-Tube Clearance Conflicts** | Structural interference between swinging tube profiles and internal L-plates. | Extended the vertical output spindle, completely raising the main rotor clear of the lower frame. |
| **Excessive Frictional Losses** | High contact resistance at high-speed gear-mesh boundaries. | Introduced an optimized lubrication maintenance schedule. |

---

## ✨ Key Advantages

* **Grid Independent:** Operates 100% on mechanical energy—zero batteries, grid lines, or generators required.
* **Low Cost & High Durability:** Constructed primarily from durable, simple mechanical metals and modular, replaceable elements.
* **Excellent Performance:** Hand-driven input easily scales up to professional diagnostic RPM benchmarks via the $81\times$ drivetrain.
* **Dual-Drive Adaptation Ready:** Designed with a modular configuration that allows the manual handle to be swapped for a small electric motor if power infrastructure becomes available later.

---

## 🔮 Future Scope

* **Velocity Governance:** Integrate a low-cost mechanical governor or centrifugal brake to cap top speeds and ensure steady, repeatable testing runs.
* **Integrated Diagnostics:** Add a simple, self-powered magnetic tachometer or mechanical counter to display real-time RPM to the laboratory technician.
* **Weight Optimization:** Exchange heavy steel structural supports for lightweight alloy or rugged polymer composite materials to improve device portability.

---

## 👥 Project Team & Acknowledgments

### Group 22 - TA212
* **Anand Sachan** (Roll No: 240116)
* **Muhammad Ubaidullah** (Roll No: 240667)
* **Yash Jaiswal** (Roll No: 241196)
* **Ayan Abbas** (Roll No: 240235)
* **Ritham Sharma** (Roll No: 240875)
* **Vishal Singh** (Roll No: 221207)
* **Sravaan Suryadevara** (Roll No: 241040)

### Instructional & Support Team
* **Course Instructor:** Dr. Sarvesh Mishra
* **Project Tutor & Guide:** Rahul Sir
* **Lab In-Charge:** Aman Singh
* **Workshop Staff:** Heartfelt thanks to the entire TA212 Lab Staff and Workshop Technicians for their outstanding manufacturing guidance and operational support.
