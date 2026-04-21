# Strix

[![PyPI version](https://badge.fury.io/py/strix.svg)](https://badge.fury.io/py/strix)
[![Python Versions](https://img.shields.io/pypi/pyversions/strix.svg)](https://pypi.org/project/strix/)
[![License](https://img.shields.io/github/license/yourusername/strix)](LICENSE)
[![Build](https://github.com/yourusername/strix/actions/workflows/build-release.yml/badge.svg)](https://github.com/yourusername/strix/actions/workflows/build-release.yml)

A powerful and extensible Python toolkit — fork of [usestrix/strix](https://github.com/usestrix/strix) with additional features and improvements.

## Features

- 🚀 Fast and lightweight
- 🔧 Highly configurable
- 🧩 Extensible plugin architecture
- 📦 Easy to install and use
- 🐍 Python 3.9+ support

## Installation

```bash
pip install strix
```

Or using [Poetry](https://python-poetry.org/):

```bash
poetry add strix
```

## Quick Start

```python
import strix

# Initialize and use strix
client = strix.Client()
client.run()
```

## Usage

### Basic Example

```python
from strix import Client, Config

config = Config(
    verbose=True,
    timeout=30,
)

client = Client(config=config)
result = client.process("your input here")
print(result)
```

### Advanced Configuration

```python
from strix import Client
from strix.config import Config

config = Config.from_file("strix.toml")
client = Client(config=config)
```

## Configuration

Strix can be configured via:

1. **Python API** — pass a `Config` object directly
2. **TOML file** — create a `strix.toml` in your project root
3. **Environment variables** — prefix with `STRIX_`

| Option | Default | Description |
|--------|---------|-------------|
| `verbose` | `False` | Enable verbose logging |
| `timeout` | `30` | Request timeout in seconds |
| `retries` | `3` | Number of retry attempts |

## Development

See [CONTRIBUTING.md](CONTRIBUTING.md) for development setup and contribution guidelines.

```bash
# Clone the repo
git clone https://github.com/yourusername/strix.git
cd strix

# Install dependencies
make install

# Run tests
make test

# Run linting
make lint
```

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes.

## License

This project is licensed under the terms of the [LICENSE](LICENSE) file.

## Acknowledgements

This project is a fork of [usestrix/strix](https://github.com/usestrix/strix). Thanks to the original authors for their work.
