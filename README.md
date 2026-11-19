# Reward Well PCB

KiCad PCB design for the reward well board used in NeuroACT behavioural neuroscience experiments. It connects to the [ECU Interface PCB](https://github.com/NeuroACT-NCBS/ECU-interface-PCB) over USB-A.

The board is about 49.5 x 21.5 mm. It carries LEDs, an ultrasonic speaker, an IR LED and photodiode pair, and SMA coaxial connectors.

## Requirements

- [KiCad](https://www.kicad.org/) 10.0+
- [NeuroACT-KiCad-libraries](https://github.com/NeuroACT-NCBS/NeuroACT-KiCad-libraries), installed as global libraries (see below)

## Setup

Clone this repository and the library repository:

```bash
git clone https://github.com/NeuroACT-NCBS/Reward-well-PCB.git
git clone https://github.com/NeuroACT-NCBS/NeuroACT-KiCad-libraries.git
```

Then add the library to KiCad as a global library:

1. In KiCad, open **Preferences → Manage Symbol Libraries**, choose the **Global Libraries** tab, and add `NeuroACT.kicad_sym` from the library clone with the nickname `NeuroACT`.
2. Open **Preferences → Manage Footprint Libraries**, choose the **Global Libraries** tab, and add the `NeuroACT.pretty` folder from the library clone with the nickname `NeuroACT`.
3. Open **Preferences → Configure Paths** and add a variable named `NEUROACT_LIBS` set to the library clone folder (the one containing `3D models/`). It is used to load the 3D models.
4. Restart KiCad and open `reward-well-pcb.kicad_pro`.

See the [library README](https://github.com/NeuroACT-NCBS/NeuroACT-KiCad-libraries#installation-as-a-global-library) for details and for editing the global library tables directly.

## Manufacturing

`gerber_to_order/` contains the Gerber files zipped for ordering from JLCPCB.

## License

CERN Open Hardware Licence Version 2 — see [LICENSE](LICENSE)
