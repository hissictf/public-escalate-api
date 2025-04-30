# public-escalate-api

A lightweight RESTful API for managing escalator state, telemetry, and emergency operations in smart building environments.

Developed by **HISSICTF Labs**, this service was part of an experimental building automation suite designed to interface with embedded control systems and provide remote diagnostics and control capabilities.

> ⚠️ This repository was published for archival/testing purposes only. It is **not intended for deployment** in live environments without thorough security review.

---

## Overview

The `public-escalate-api` exposes control and monitoring functions for escalator units connected via a standard MQTT/REST bridge. It was built to support remote operations, including:

- Monitoring escalator operational status (run, idle, fault)
- Sending emergency stop or reset commands
- Collecting usage metrics (cycle count, run time)
- Integration with smart building dashboards

Originally tested in controlled environments with simulated PLC backends.

---

## Features

- Lightweight FastAPI backend
- MQTT integration via `paho-mqtt`
- Optional authentication middleware (not enabled by default)
- Dockerized deployment for lab environments
- CLI tools for basic admin tasks

---

## Quickstart

Use the included `docker-compose.yml` to spin up the service alongside a mock MQTT broker.

```bash
docker-compose up -d
