# HackBoard-v4.0

A custom 75% mechanical gaming keyboard featuring a Raspberry Pi Pico 2 microcontroller, VIA keyboard configurator support, and a rotary encoder for media control. This project combines elegant PCB design, modular mechanical construction, and open-source firmware for a fully customizable typing experience.

## Features

- **75% Layout**: 81 keys in a compact form factor with dedicated function row and arrow cluster
- **Microcontroller**: Raspberry Pi Pico W with VIA firmware support for real-time key remapping
- **Rotary Encoder**: Integrated media control knob (volume, track navigation)
- **Hot-Swap Compatible**: Cherry MX switch sockets for easy customization
- **Modular Mechanical Design**: Separate PCB, plate, case, and top cover for assembly flexibility
- **Full Diode Matrix**: Per-key diodes for reliable switch detection across all 81 keys
- **Open Source**: Schematics, PCB design files, and production assets included

## Electronics Design

The HackBoard v4.0 uses a matrix-based keyboard design with a Raspberry Pi Pico W as the main controller. Each switch connects to the microcontroller through a matrix circuit, with individual SOD-123 diodes preventing ghosting and ensuring reliable key registration.

![Schematic showing microcontroller and switch matrix connections](images/Screenshot%202026-02-04%20210234.png)

The circuit is optimized for minimal latency and power efficiency, with the Pico's USB connectivity enabling VIA firmware for instant key remapping without recompilation.

![Matrix layout and electrical connections](images/Screenshot%202026-02-04%20212200.png)

![Detailed schematic routing for power distribution and signal integrity](images/Screenshot%202026-02-04%20212823.png)

## PCB Design

The PCB is a carefully routed four-layer board that integrates the switch matrix, microcontroller, and rotary encoder in a compact 75% layout. Signal integrity and ground plane continuity were prioritized for minimal EMI and stable operation.

![PCB Layout - Component Placement Layer](images/Screenshot%202026-02-04%20213837.png)

![PCB Layout - Top Signal Layer with trace routing](images/Screenshot%202026-02-04%20214133.png)

![PCB Layout - Bottom Signal Layer showing efficient routing](images/Screenshot%202026-02-04%20214225.png)

![PCB 3D visualization showing component heights and assembly clearance](images/Screenshot%202026-02-04%20214312.png)

The design includes mounting points for the stabilizers, hotswap sockets for all key positions, and a dedicated encoder footprint. Via stitching around signal traces ensures proper grounding.

![PCB Assembly Layout with component designators](images/Screenshot%202026-02-04%20214339.png)

![Finished PCB layout ready for fabrication](images/Screenshot%202026-02-04%20214610.png)

## Mechanical Design

### Plate Design

The plate provides structural rigidity and supports the stabilizers while maintaining compatibility with Cherry MX switches across all positions.

![Plate Assembly - Engineering drawing and mounting holes](images/Screenshot%202026-02-04%20214638.png)

### Case Design

The case forms the keyboard body and houses the PCB, plate, stabilizers, and all mounting hardware. The design balances acoustics, durability, and aesthetic appeal.

![Case - 3D CAD render showing overall form and enclosure](images/Screenshot%202026-02-04%20214841.png)

![Case - Bottom detail showing mounting features](images/Screenshot%202026-02-04%20214937.png)

### Top Cover

The polycarbonate top cover provides a transparent view of the PCB and components while protecting them from dust and accidental contact.

![Top Cover Assembly - 3D visualization](images/Screenshot%202026-02-05%20151252.png)

![Top Cover - Detailed assembly view](images/Screenshot%202026-02-05%20152425.png)

## Final Assembly & Look

The fully assembled HackBoard v4.0 showcases the integration of all mechanical and electrical components into a cohesive, functional design. The transparent top cover highlights the clean PCB layout and component quality.

![Keyboard Assembly - Front view showing key layout](images/Screenshot%202026-02-05%20152441.png)

![Keyboard Assembly - Top detail with rotary encoder visible](images/Screenshot%202026-02-05%20162554.png)

![Keyboard - Side profile showing case thickness and profile](images/Screenshot%202026-02-05%20163222.png)

![Keyboard - 3D render showing final aesthetic](images/Screenshot%202026-02-05%20163355.png)

![Keyboard - Angled view highlighting PCB visibility through top cover](images/Screenshot%202026-02-05%20163637.png)

![Keyboard - Bottom view showing mounting and cable routing](images/Screenshot%202026-02-05%20163813.png)

## Bill of Materials

| Component Name | Qty | Price (₹) | Price ($) | Vendor |
|---------------|-----|-----------|-----------|--------|
| Raspberry Pi Pico 2 / Pico 2 W | 1 | ₹635 | $8.00 | [Robu.in](https://robu.in/) |
| Custom 75% Keyboard PCB | 1 | ₹4,692 | $52.00 | [PowerPCB](https://powerpcb.com/) |
| MX Mechanical Switches (Akko V5) | 84 | ₹2,398 | $27.00 | [StacksKB](https://stackskb.com/store/akko-v5-creamy-yellow-pro-switch-pack-of-45/) |
| Clear Screw-In Stabilizer | 4 + 1 (6.25U) | ₹1,595 | $18.00 | [StacksKB](https://stackskb.com/store/durock-clear-screw-in-stabilizers-v2/?attribute_combination=4%2B1+Set&attribute_spacebar-size=6.25U) |
| 1N4148W Diodes (SOD-123) | 84 | ₹122 | $1.50 | [Robu.in](https://robu.in/) |
| Rotary Encoder (with push button) | 1 | ₹55 | $1.00 | [Robu.in](https://robu.in/product/hongyan-ec11h-7ce15p1zd15f7-rotary-encoder-with-push-button-switch-vertical-plug-in-5-pin-360-degree/) |
| Keycap Set (75% compatible) | 1 set | ₹2,399 | $27.00 | [Robu.in](https://robu.in/) |
| M2.5 Screws | 7 | ₹43.30 | $0.50 | [OnlyScrews.in](https://onlyscrews.in/) |
| M2.5 Heat-set Inserts | 7 | ₹14.00 | $0.20 | [OnlyScrews.in](https://onlyscrews.in/) |
| M1.6 Screws | 5 | ₹16.00 | $0.20 | [OnlyScrews.in](https://onlyscrews.in/) |
| Shipping (Robu.in) | 1 | ₹49 | $0.59 | [Robu.in](https://robu.in/) |
| Shipping (OnlyScrews.in) | 1 | ₹60 | $0.72 | [OnlyScrews.in](https://onlyscrews.in/) |

---

## Total Cost

**Total (INR): ₹12,078.30**  
**Total (USD): $136.71**

## Project Files

```
PCB/
├── HackBoard v4.kicad_sch    # KiCad schematic
├── HackBoard v4.kicad_pcb    # KiCad PCB layout
├── HackBoard v4.kicad_pro    # KiCad project settings

CAD/
├── Case.step                 # Case 3D model (STEP format)
├── plate.step                # Plate 3D model (STEP format)
├── Top Cover.step            # Top cover 3D model (STEP format)

production/
├── bom.csv                   # Bill of Materials
├── designators.csv           # Component designators
├── positions.csv             # Pick-and-place coordinates
└── netlist.ipc               # IPC netlist format
```

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
