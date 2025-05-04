---
layout: default
title: "Building a Triangle Core VCO"
---

<script type="text/javascript" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# Building a Triangle Core VCO

This is a simple documentation of how I built a triangle core voltage-controlled oscillator inspired by the Buchla 259.

## Circuit Theory

The oscillator core is based on an op-amp integrator with a comparator feedback loop.

The triangle output frequency is derived as:

$$
f = \frac{I}{2VC}
$$

Where:
- \( I \) is the current into the integrator,
- \( V \) is the amplitude swing,
- \( C \) is the integration capacitor.

## Design Decisions

- Core architecture: Schmitt-trigger with precision current source
- Temperature compensation: Tempco resistor on expo converter
- Waveshaping: Sine shaper via differential pair

## Scope Traces

![Triangle wave](./images/triangle_scope.jpg)


| Component | Value |
|----------|-------|
| Op-Amp   | TL072 |
| Capacitor C1 | 1nF |

## Audio Sample

<audio controls>
  <source src="vco_output.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
