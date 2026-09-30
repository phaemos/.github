# PHAEMOS

**Reveal before failure.** An open industrial IoT platform for predictive maintenance: sensor nodes stream what a machine is doing, a live dashboard shows it and machine learning flags the anomaly before it becomes a breakdown.

The name is pronounced FAY-mos and means "an ordered system that reveals".

- **Four sensor nodes:** an ESP32 gateway with 11 sensors, an STM32 running vibration FFT at 100 Hz, an Arduino Nano and a Raspberry Pi Pico 2W
- **Real-time pipeline:** FastAPI ingest, PostgreSQL and Redis, WebSocket streaming to a Next.js dashboard
- **Anomaly detection:** an Isolation Forest scores every reading as it arrives and opens a ticket when a machine drifts
- **Operations built in:** alert rules, maintenance windows, tickets, webhooks, audit logging and role-based access
- **Resilient at the edge:** a Rust gateway spools readings to disk, so a network outage loses nothing

## Repositories

| Repository | What it is |
| --- | --- |
| [phaemos](https://github.com/phaemos/phaemos) | The monorepo where all development happens. Start here |
| [backend](https://github.com/phaemos/backend) | FastAPI ingest, alerting, tickets and anomaly scoring |
| [frontend](https://github.com/phaemos/frontend) | Next.js live monitoring dashboard |
| [firmware](https://github.com/phaemos/firmware) | Firmware for the ESP32, STM32, Arduino Nano and Pico 2W nodes |
| [hardware](https://github.com/phaemos/hardware) | Schematics, PCB notes, wiring and parts |
| [infra](https://github.com/phaemos/infra) | Docker Compose stack, monitoring and reporting SQL |
| [client](https://github.com/phaemos/client) | Python SDK, telemetry simulator and the `phaemosctl` Go tool |
| [edge](https://github.com/phaemos/edge) | Rust store-and-forward gateway |

Every component repository is a read-only copy published from the monorepo. Issues, discussions and pull requests all go to [phaemos/phaemos](https://github.com/phaemos/phaemos).

## Links

[phaemos.com](https://phaemos.com) · [Documentation](https://docs.phaemos.com) · [Status](https://status.phaemos.com) · [Discussions](https://github.com/phaemos/phaemos/discussions)
