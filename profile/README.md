<h1 align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/phaemos/phaemos/main/assets/brand/phaemos-logo-dark.png">
    <img src="https://raw.githubusercontent.com/phaemos/phaemos/main/assets/brand/phaemos-logo-light.png" alt="PHAEMOS: reveal before failure" width="300">
  </picture>
</h1>

**Reveal before failure.** An open industrial IoT platform for predictive maintenance: sensor nodes stream what a machine is doing, a live dashboard shows it and machine learning flags the drift before it becomes a breakdown.

The name is pronounced FAY-mos and means "an ordered system that reveals".

- **Four sensor nodes:** an ESP32 gateway with 11 sensors, an STM32 running a vibration FFT at 100 Hz, an Arduino Nano and a Raspberry Pi Pico 2W
- **Real-time pipeline:** FastAPI ingest, PostgreSQL and Redis, WebSocket streaming to a Next.js dashboard
- **Anomaly detection:** an Isolation Forest scores every reading as it arrives and raises an alert when a machine drifts
- **Operations built in:** alert rules, maintenance windows, tickets, webhooks, email and SMS, audit logging and role-based access
- **Resilient at the edge:** a Rust gateway spools readings to disk, so a network outage loses nothing
- **Tools for developers:** a Python SDK, a simulator with injectable faults and a Go CLI for load testing
- **Open hardware and software:** CERN-OHL-S hardware designs, AGPL code, self-hosted with Docker Compose

> [!NOTE]
> The software runs end to end today, with a simulator standing in for real machines. Wiring the nodes, training the model on real readings and launching phaemos.com come next. Follow along on the [roadmap](https://github.com/orgs/phaemos/projects/1).

## Roadmap

| Milestone | What it covers |
| --- | --- |
| [Verify: full local test](https://github.com/phaemos/phaemos/milestone/1) | The whole stack run locally, every page walked end to end |
| [Community: Discord server](https://github.com/phaemos/phaemos/milestone/2) | A scripted Discord server for support, each board and show and tell |
| [Launch: external services](https://github.com/phaemos/phaemos/milestone/3) | The API, dashboard, docs and status page online, with email, SMS and social sign-in |
| [Hardware: physical nodes](https://github.com/phaemos/phaemos/milestone/4) | Every sensor tested on real machines, the model trained on that data, then PCBs and enclosures |

## Tech stack

Python (FastAPI, SQLAlchemy, scikit-learn) and TypeScript (Next.js, Tailwind CSS) for the platform. C and C++ on the ESP32, STM32 and Nano, MicroPython on the Pico 2W. Rust for the edge gateway and Go for `phaemosctl`. PostgreSQL, Redis and Docker underneath.

## Repositories

| Repository | What it is |
| --- | --- |
| [phaemos](https://github.com/phaemos/phaemos) | The monorepo where all development happens. Start here |
| [backend](https://github.com/phaemos/backend) | FastAPI ingest, alerting, tickets and anomaly scoring |
| [frontend](https://github.com/phaemos/frontend) | Next.js live monitoring dashboard |
| [firmware](https://github.com/phaemos/firmware) | Firmware for the ESP32, STM32, Arduino Nano and Pico 2W nodes |
| [hardware](https://github.com/phaemos/hardware) | Wiring tables, schematics, PCB layouts and the parts inventory |
| [edge](https://github.com/phaemos/edge) | Rust store-and-forward gateway |
| [client](https://github.com/phaemos/client) | Python SDK, telemetry simulator and the `phaemosctl` Go tool |
| [infra](https://github.com/phaemos/infra) | Docker Compose stack, monitoring and reporting SQL |

Every component repository is a read-only copy published from the monorepo. Issues, discussions and pull requests all go to [phaemos/phaemos](https://github.com/phaemos/phaemos).

## Get involved

- **Start here:** the [welcome post](https://github.com/phaemos/phaemos/discussions/133) and the [roadmap post](https://github.com/phaemos/phaemos/discussions/284)
- **Questions and ideas:** [Discussions](https://github.com/phaemos/phaemos/discussions), with [Q&A](https://github.com/phaemos/phaemos/discussions/categories/q-a) for help and [Ideas](https://github.com/phaemos/phaemos/discussions/categories/ideas) for suggestions
- **Bugs and feature requests:** [issues on the monorepo](https://github.com/phaemos/phaemos/issues/new/choose)
- **What is coming:** the [roadmap board](https://github.com/orgs/phaemos/projects/1) and the [milestones](https://github.com/phaemos/phaemos/milestones)
- **Contributing:** the [contributing guide](https://github.com/phaemos/phaemos/blob/main/CONTRIBUTING.md)
- **Security:** report vulnerabilities privately through the [security policy](https://github.com/phaemos/phaemos/security/policy)
- **Contact:** [contact@phaemos.com](mailto:contact@phaemos.com)
