# 🌱 Planetary Remediation Swarm

[![CI](https://github.com/GALACTIC-UNION/planetary-remediation-swarm/actions/workflows/ci.yml/badge.svg)](https://github.com/GALACTIC-UNION/planetary-remediation-swarm/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Python 3.12+](https://img.shields.io/badge/python-3.12%2B-blue)](https://www.python.org/)

**Coordinated multi-agent remediation of polluted environments** — combining
robotics, bio-agents, and chemical neutralisation in a unified orchestration layer.
Part of the OCN GAIA-NANO domain.

---

## Overview

Planetary Remediation Swarm (PRS) is an orchestration platform that coordinates
heterogeneous remediation agents (autonomous robots, microbial applicators,
chemical dosing units) to address large-scale environmental contamination.
It ingests telemetry data, classifies contamination events, generates remediation
plans, and tracks execution to completion.

### Key Capabilities

| Capability | Description |
|---|---|
| **Contamination classification** | ML pipeline for pollutant identification from spectral/sensor data |
| **Swarm task planning** | Multi-agent task allocation using auction-based algorithms |
| **Agent communication** | MQTT-based mesh for real-time command & telemetry |
| **Progress tracking** | Mission state machine with rollback and replanning |
| **Reporting** | Automated remediation reports with before/after comparisons |

---

## Quick Start

```bash
git clone https://github.com/GALACTIC-UNION/planetary-remediation-swarm.git
cd planetary-remediation-swarm
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
cp config/config.example.yaml config/config.yaml
python src/orchestrator/main.py
```

## Project Structure

```
planetary-remediation-swarm/
├── src/
│   ├── orchestrator/     # Mission planning and agent coordination
│   ├── classification/   # Pollutant detection ML models
│   ├── comms/            # Agent communication layer (MQTT)
│   ├── planning/         # Task allocation algorithms
│   └── reporting/        # Mission reports and analytics
├── docs/
│   ├── architecture.md
│   ├── agent-protocol.md
│   └── deployment-guide.md
├── tests/
├── config/
├── .github/workflows/ci.yml
├── requirements.txt
├── CONTRIBUTING.md
└── README.md
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — see [LICENSE](LICENSE).
