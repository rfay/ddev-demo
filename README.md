[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/rfay/ddev-demo/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/rfay/ddev-demo/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/rfay/ddev-demo)](https://github.com/rfay/ddev-demo/commits)
[![release](https://img.shields.io/github/v/release/rfay/ddev-demo)](https://github.com/rfay/ddev-demo/releases/latest)

# DDEV Demo

## Overview

This add-on integrates Demo into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get rfay/ddev-demo
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Demo |
| `ddev logs -s demo` | Check Demo logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.demo --demo-docker-image="ddev/ddev-utilities:latest"
ddev add-on get rfay/ddev-demo
ddev restart
```

Make sure to commit the `.ddev/.env.demo` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `DEMO_DOCKER_IMAGE` | `--demo-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@rfay](https://github.com/rfay)**
