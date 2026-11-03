# Field notes

These notes summarize observations from October 2026. The head unit and vehicle configuration were not rechecked when this repository was prepared; treat configuration details as historical.

## Setup

- Vehicle: 2010 UK Honda Civic Type R (FN2).
- Head unit: K706, Android 10 / API 29.
- The head unit uses QF software and a Raise CAN box in the observed setup.

## CAN profile and climate data

- The profile catalog had Civic Type R 08–10 Low and High entries, but no explicit FN2, UK, FD2, or Japan profile. Those entries are the closest catalog matches, not confirmed compatibility.
- Multiple profiles were tried during investigation. The final intended profile was not verified, so no profile should be assumed current or recommended from these notes.
- In an unfiltered trace, fan-speed changes were reflected in received climate data. Temperature and recirculation changes produced no visible corresponding change in that trace.
- This only describes the tested configuration and trace. It does not prove that the vehicle produces no temperature or recirculation signal, or that the CAN box is defective.
- Shared QF interfaces expose generic climate data and controls. Their presence does not establish that the selected FN2 profile supports those functions.

## USB volume knob

- Rotation produced Android volume-up and volume-down key events. A per-device key layout mapped those to QF volume controls; pressing the knob triggered QF mute.
- Next-track reached the QF layer as an unknown key and was not remapped.

## Companion apps

- **CRAB ECT Bridge:** reads CRAB's existing coolant-temperature broadcasts and forwards the reading to the K706 status bar. The bridge is opt-in and does not open its own OBD, Bluetooth, CAN, or MCU connection. See its README for behavior and limitations.
- **YouTube Music Bridge:** reads the active media session and can forward metadata to the QF display. Forwarding defaults to off. The source is a prototype; display-source labeling is not verified.

The bridge source is maintained in the linked app repositories. No vendor application binaries or decompiled source are included here.

## Limits and next evidence

- Findings are specific to the observed head unit, CAN box, vehicle, and configuration; other FN2/K706 installations may differ.
- No raw CAN capture is included. A passive capture under a confirmed profile would be needed before drawing broader conclusions about climate signals.
- Factory codes, command payloads, firmware/update procedures, and device dumps are intentionally omitted.
