# Non_overlapping_clock
# 🕒 Non-Overlapping Clock Generators (2-Phase & 3-Phase) – CMOS Design in Tanner EDA

##  What is a Non-Overlapping Clock?

A **non-overlapping clock** system generates multiple clock phases such that no two clocks are high at the same time. This prevents charge sharing and ensures proper signal settling in **switched-capacitor circuits**, **sample-and-hold circuits**, and **correlated double sampling (CDS)** applications.

In 2-phase and 3-phase systems, each clock phase is separated by a small intentional delay (non-overlap window), which is critical in analog circuits to avoid simultaneous switch activation.

---

##  Purpose of the Design

This project implements **2-phase and 3-phase non-overlapping clock generators** using **CMOS logic** in **Tanner EDA** (S-Edit for schematics and T-Spice for simulation). These designs are crucial components of an upcoming **Data Acquisition System (DAQ)** project, ensuring accurate and clean sampling.

---

##  Gate-Level CMOS Design

To build the clock generators from scratch, the following CMOS logic gates were designed and sized manually:

- **CMOS Inverter** – Designed for deliberate propagation delay
- **CMOS NOR Gate**
- **CMOS NAND Gate**

MOSFET sizing (PMOS & NMOS) was carefully adjusted to achieve a **targeted delay of ~2ns** between clock transitions.

---

##  Design Highlights

- **2-Phase Non-Overlapping Clock**: Two complementary clocks with a 2 ns gap to avoid overlap.
- **3-Phase Non-Overlapping Clock**: Three periodic pulses spaced such that no two phases overlap.
- **Delay Insertion**: Multiple inverter stages were intentionally inserted to create delay between transitions.
- **Custom MOS Sizing**: PMOS and NMOS widths were fine-tuned to control rise/fall times and ensure precise phase delay.

---



