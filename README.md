# Honda FN2 / K706 head-unit research

Read-only notes from investigating an aftermarket K706 Android head unit in a 2010 UK Honda Civic Type R (FN2). The notes distinguish observed behavior from assumptions and are not a vehicle repair or CAN-bus control guide.

## Contents

- [`docs/field-notes.md`](docs/field-notes.md) — device context, findings, limits, and open questions.
- [`apps/crab-ect-bridge`](apps/crab-ect-bridge) — companion repository for the opt-in CRAB coolant-temperature display bridge.
- [`apps/ytmusic-bridge`](apps/ytmusic-bridge) — companion repository for the source-only YouTube Music metadata bridge.

The app directories are Git submodules. Clone with `git clone --recurse-submodules` to check them out. They also remain available as standalone repositories: [crab-ect-bridge](https://github.com/Rashoooodi/crab-ect-bridge) and [ytmusic-bridge](https://github.com/Rashoooodi/ytmusic-bridge).

## Public-repository scope

This repository contains original notes and links to the companion app source. It does not redistribute QF, Android, Agama, or other vendor APKs; framework or firmware files; decompiled vendor source; raw device dumps or logs; private configuration backups; or factory/service codes. Those files may contain third-party material, device-specific identifiers, or settings that should not be copied into a public repository.

No license for reuse is provided at this time.
