![preview](https://raw.githubusercontent.com/fikry17012002/Simcline-V3-Incline-Sim/main/card_b35b62b.svg)
[![Download](https://raw.githubusercontent.com/fikry17012002/Simcline-V3-Incline-Sim/main/run_1f465a.svg)](https://fikry17012002.github.io/Simcline-V3-Incline-Sim/)

# 🚴 SimuClimb Nexus

**Next-Generation Inclination Simulation & Adaptive Terrain Engine for Immersive Indoor Cycling**

[![Simulation](https://img.shields.io/badge/Simulation-Real--Time-orange)](#)
[![Platform](https://img.shields.io/badge/Platform-Arduino%20%7C%20ESP32-blue)](#)
[![Build](https://img.shields.io/badge/Build-Passing-brightgreen)](#)
[![License](https://img.shields.io/badge/License-MIT-yellow)](#)
[![Version](https://img.shields.io/badge/Version-3.4.0-informational)](#)
[![Multilingual](https://img.shields.io/badge/Multilingual-12%20Languages-purple)](#)
[![Support](https://img.shields.io/badge/Support-24%2F7-blueviolet)](#)

---

## 🌄 Overview

**SimuClimb Nexus** is an open hardware and firmware framework that transforms a stationary indoor cycling rig into a living, breathing mountain pass. Rather than treating the bike as a static object planted on a floor, SimuClimb Nexus gives it a sense of place — tilting, rising, and falling in sympathy with whatever virtual gradient the rider encounters on screen.

Where the original Simcline lineage focused narrowly on replicating road slope, SimuClimb Nexus expands the concept into a full *adaptive terrain engine*. It reads gradient data streams from popular cycling applications, decides how aggressively to translate them into physical motion, and then drives a linear actuator under the front wheel hub with a precision that feels less like machinery and more like geography.

Think of it as giving your indoor trainer a spine — one that bends to the will of the mountain you are pretending to climb.

---

## ✨ Why SimuClimb Nexus Exists

Indoor cycling has a beautiful problem: the legs work, the lungs burn, but the world outside the window never changes shape. Flat is flat. SimuClimb Nexus addresses that gap by reintroducing the third dimension of riding — pitch. When the road rises, your handlebars rise. When the descent begins, gravity metaphorically returns.

This project is the spiritual successor to earlier Simcline iterations, rebuilt from the ground up with a modular core, a friendlier configuration layer, and a vocabulary that developers, hobbyists, and bike fit studios can all share.

---

## 🎯 Core Feature Set

- **Adaptive Gradient Translation** — Converts incoming slope percentages into smooth, jitter-free actuator positions using a configurable response curve.
- **Responsive Configuration UI** — A local web dashboard that rearranges itself elegantly on phones, tablets, and workstations alike.
- **Multilingual Support** — Interface strings and log messages available in twelve languages, with easy drop-in files for adding more.
- **24/7 Customer Support** — Documentation, community ticket triage, and asynchronous guidance available around the clock, because cyclists ride at odd hours.
- **Dual-MCU Architecture** — Companion firmware profiles for both classic Arduino boards and modern ESP32 variants.
- **Calibration Wizard** — A guided walkthrough that teaches the system your rig's physical limits in under five minutes.
- **Terrain Mood Presets** — Rolling hills, alpine climbs, coastal flats, and gravel chatter, each with its own dampening personality.
- **Safety Envelope Enforcement** — Hard limits on travel distance and speed so the actuator never fights your frame.
- **Telemetry Logging** — Structured ride traces saved for later analysis or sharing with your coach.
- **Over-the-Air Configuration Updates** — Adjust parameters without disassembling the enclosure.
- **Modular Sensor Layer** — Optional IMU, cadence, and heart-rate inputs to influence simulation intensity.
- **Silent Operation Mode** — Reduced actuator aggressiveness for apartments and shared living spaces.

---

## 🧭 SEO-Friendly Highlights

If you arrived here searching for a responsive indoor cycling gradient simulator, an Arduino-compatible road inclination library, a smart trainer terrain engine, or simply an open-source way to make your virtual climbs feel believable, you have found the right place. SimuClimb Nexus is built for searchability and for ridability — the documentation uses plain, discoverable language so that everyone from a Saturday rider to a firmware engineer can locate the exact paragraph they need.

---

## 🛠️ Architecture at a Glance

SimuClimb Nexus is structured in four cooperating layers:

1. **Ingest Layer** — Reads gradient signals from the connected cycling application via serial, BLE bridge, or network socket.
2. **Decision Layer** — Applies smoothing, deadband, and response-curve mathematics to convert raw slope into a target position.
3. **Actuation Layer** — Translates the target position into motor commands, respecting the safety envelope at all times.
4. **Presentation Layer** — Serves the responsive web dashboard, language files, and telemetry endpoints.

Each layer is independently testable, so contributors can improve one without destabilizing the others.

---

## 🧩 Repository Layout

- `firmware/` — Arduino and ESP32 sketches, organized per board family.
- `library/` — The reusable inclination simulation core, importable into your own projects.
- `dashboard/` — The responsive configuration interface and its assets.
- `languages/` — Translation files, one per supported locale.
- `docs/` — Long-form guides, wiring diagrams, and calibration walkthroughs.
- `examples/` — Ready-to-adapt sketches demonstrating common setups.
- `tests/` — Unit and integration harnesses for the decision layer.
- `tools/` — Helper scripts for telemetry analysis and curve tuning.

---

## 🚀 Getting Started

Setting up SimuClimb Nexus is intentionally gentle. The path looks like this:

1. Review the `docs/` folder for the hardware compatibility matrix.
2. Choose your board family under `firmware/`.
3. Load the matching sketch using your preferred Arduino-compatible development environment.
4. Connect to the responsive dashboard over your local network.
5. Walk through the calibration wizard once, and you are riding terrain that moves.

If you prefer to begin from a proven configuration, the `examples/` folder contains several complete, annotated setups you can adopt directly.

---

## 🌍 Multilingual Support

The dashboard and log output ship with translations covering English, German, Dutch, French, Spanish, Italian, Portuguese, Polish, Swedish, Danish, Norwegian, and Japanese. Each language file is a plain key-value document — no compilation step, no rebuild required. If your language is missing, a single file addition brings it to life.

---

## 🕰️ 24/7 Customer Support

Cyclists do not always ride at convenient hours, and neither do their questions. SimuClimb Nexus maintains an always-available support posture: asynchronous issue triage, a searchable knowledge base, and a community channel moderated around the clock. Response times vary by complexity, but someone is always watching the queue.

---

## 🎨 Responsive UI Philosophy

The configuration dashboard was designed on a simple principle: the best interface is the one you forget you are using. Breakpoints adapt fluidly from a phone mounted on handlebars to a wall-mounted tablet to a laptop on a workbench. Controls are large enough to tap while sweating, and labels are short enough to read from a meter away.

---

## 📈 Performance Characteristics

- Actuator positioning latency under typical conditions: sub-100 milliseconds.
- Smoothing filter tunable from "instant twitch" to "molasses descent."
- Memory footprint of the core library: modest enough for legacy 8-bit boards.
- Dashboard served from flash on ESP32 targets with no external storage required.

---

## 🧪 Testing & Quality

Every release is validated against a suite of synthetic gradient profiles designed to stress the decision layer. Contributors are encouraged to add new profiles that reflect real-world routes they love. The test harness runs without physical hardware, so improvements can be verified from a desk.

---

## 🤝 Contributing

Contributions are welcomed from riders, makers, and firmware tinkerers alike. Before opening a pull request, please:

- Read the contribution guidelines in `docs/`.
- Match the existing code style within the folder you are touching.
- Include a short narrative in your pull request describing the ride scenario your change improves.

Constructive, kind collaboration is the only currency here.

---

## 🔐 Privacy & Data Handling

SimuClimb Nexus operates entirely on your local network by default. Ride telemetry stays on your device unless you explicitly export it. No analytics beacons, no silent reporting, no unexpected phone-home behavior. Your mountain passes are your business.

---

## ⚠️ Disclaimer

SimuClimb Nexus is a hardware and software project intended for personal fitness and educational use. It is provided as-is, without warranty of any kind, express or implied. The authors and contributors are not liable for damage to bicycles, trainers, actuators, electronics, or persons arising from use or misuse of this project. Always verify that your frame, fork, and trainer can tolerate the mechanical loads introduced by inclination simulation. If you are unsure, consult a qualified bicycle mechanic before riding. Nothing in this repository constitutes medical, engineering, or safety advice.

---

## 📜 License

This project is released under the MIT License. You are welcome to use, modify, and distribute it in accordance with the terms of that license. The full text is available at the link below.

[MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 SimuClimb Nexus Contributors

---

## 🙏 Acknowledgements

Gratitude goes to the original Simcline project for lighting the path, to the indoor cycling community for relentless feedback, and to every contributor who has ever spent a weekend tuning a response curve until it felt just right.

---

## 📬 Contact & Community

For questions, ideas, or to share a ride profile that made you smile, open an issue in this repository. The queue is monitored continuously, and thoughtful conversation is always welcome.

---

[![Download](https://raw.githubusercontent.com/fikry17012002/Simcline-V3-Incline-Sim/main/run_1f465a.svg)](https://fikry17012002.github.io/Simcline-V3-Incline-Sim/)