# openelectronics

[![Checks](https://github.com/KrunalPanchal1995/openelectronics/actions/workflows/ci.yml/badge.svg)](https://github.com/KrunalPanchal1995/openelectronics/actions/workflows/ci.yml) ![License: MIT](https://img.shields.io/badge/license-MIT-green?style=flat-square) [![Live](https://img.shields.io/badge/live-site-1f6feb?style=flat-square)](https://krunalpanchal1995.github.io/openelectronics/)

**Interactive instruments and first-principles learning pages for electrical and electronics engineering.**

- **Live site:** <https://krunalpanchal1995.github.io/openelectronics/>
- **Circuit Lab:** <https://krunalpanchal1995.github.io/openelectronics/app/>

## Circuit Lab

One self-contained page (`app/index.html`, no build step) with five instruments. Move a slider and watch the textbook formula's answer move.

| Instrument | Link | What it shows |
|---|---|---|
| RLC and phasors | [`#rlc`](https://krunalpanchal1995.github.io/openelectronics/app/#rlc) | current vs frequency, f₀ = 1/(2π√LC), Q, bandwidth, phasor diagram |
| Bode plots | [`#bode`](https://krunalpanchal1995.github.io/openelectronics/app/#bode) | first and second order low-pass, high-pass, band-pass; gain, phase, -3 dB point |
| Smith chart | [`#smith`](https://krunalpanchal1995.github.io/openelectronics/app/#smith) | reflection coefficient, VSWR, return loss, mismatch loss, impedance along a lossless line |
| Diode and MOSFET | [`#dev`](https://krunalpanchal1995.github.io/openelectronics/app/#dev) | Shockley diode with load line; square-law MOSFET output curves |
| Buck and boost | [`#dcdc`](https://krunalpanchal1995.github.io/openelectronics/app/#dcdc) | output voltage, ripple, critical inductance, inductor-current waveform |

Models: lumped RLC, Shockley diode (I_S = 1 pA, 300 K), square-law MOSFET with channel-length modulation, lossless transmission line, ideal switches. For learning and for checking hand calculations, not for design sign-off. The formulas were checked against independent Python calculations.

## Learning pages

Ten pages, each with intuition, school, college and advanced levels, worked examples, two figures computed from the formulas, and questions with answers. Notes are in `course/<topic>/notes.md`.

- **Photonics:** electromagnetics and Maxwell; silicon photonics waveguides; lasers and photodetectors.
- **Chips and devices:** IC fabrication flow; lithography and EUV limits; MOSFET and CMOS scaling; VLSI circuit design.
- **Power, RF and sensing:** power electronics converters; RF, antennas and microwaves; sensors, MEMS and control.

## Regenerate the figures

```bash
python -m pip install -r requirements.txt
python codes/make_ee_figures.py     # writes course/<topic>/figures/*.png and codes/ee_figures_manifest.json
```

Illustrative parameters are labelled "illustrative" on the figures.

Main site: <https://krunalpanchal1995.github.io/projects/electronics-lab/>. MIT licence.
