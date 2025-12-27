☀️ Tiny Solar Power Supply 🔋
An ultra-compact solar-powered DC supply for low-power electronics, sensors, and hobby projects.

Tiny Solar Power Supply is a small, efficient power module that takes energy from a mini solar panel and delivers a stable regulated output for your circuits. It is ideal for IoT nodes, garden lights, and always-on sensor projects where wiring a mains adapter is not practical.

✨ Key Features
🔌 Wide input range: Works from small solar panels (approx. 1–5 V)

⚡ Regulated output: Boost converter provides stable 3.3 V or 5 V (up to ~350 mA)

🔁 Smart power path: Prioritizes solar energy when available

🧩 Compact footprint: 2-layer PCB optimized for easy integration into enclosures

🛠 KiCad-based design: Fully open-source schematic and layout for learning and modification

🛠 Technical Specifications
| Item               | Specification                                    |
| ------------------ | ------------------------------------------------ |
| Input source       | Small solar panel (1–5 V)                        |
| Output voltage     | 3.3 V or 5 V (set by feedback resistors)         |
| Regulator IC       | AP3015 (or equivalent boost converter)           |
| Max output current | Up to ~350 mA (depending on input source)        |
| PCB                | 2‑layer, compact layout, through‑hole connectors |

📦 Repository Structure
├── Hardware/
│   ├── KiCad/
│   │   ├── tiny_solar_power_supply.kicad_sch
│   │   └── tiny_solar_power_supply.kicad_pcb
│   ├── Gerbers/
│   │   ├── *.gbr
│   │   └── *.drl
│   └── 3D/
│       └── tiny_solar_power_supply.step
│
├── Assembly/
│   ├── BOM.csv
│   └── tiny_solar_power_supply-pos.csv
│
├── Docs/
│   ├── Tiny_Solar_Power_Supply_Schematic.pdf
│   └── Tiny_Solar_Power_Supply_Overview.md
│
├── Images/
│   ├── TOP_VIEW.png
│   ├── BOTTOM_VIEW.png
│   └── 3D_RENDER.png
│
├── Examples/
│   └── Basic_Connection_Diagram.md
│
├── README.md
└── LICENSE.md

🔧 How it Works
☀️ Daytime (Charging mode)
Solar panel voltage is high. Current flows through the protection diode.
The boost converter is mostly disabled to reduce losses.

🌙 Nighttime (Power mode)
When solar voltage drops, the circuit automatically switches.
The boost converter turns ON, stepping up to stable 3.3 V / 5 V output.

🚀 Getting Started
Prerequisites
A small solar panel (e.g., 3–6 V)

Basic electronics tools for soldering and testing (multimeter, USB power meter, etc.)

Build & Order
Open the KiCad project in the Hardware/KiCad folder.

Generate or use the provided Gerber files in Gerbers/ for PCB manufacturing.

Order boards from JLCPCB, PCBWay, or any other PCB manufacturer.

Use BOM.csv and Tiny_Solar_Power_Supply-pos.csv for assembly services.

Basic Usage
Connect the solar panel to the SOLAR IN pads.

Take regulated power from the VOUT and GND pins.

Optionally use the on‑board switch to turn the output on/off.
