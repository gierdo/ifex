# Migration from setuptools to uv

This project has been migrated from setuptools with requirements.txt to uv with pyproject.toml for better dependency management and development experience.

## What Changed

- **Removed**: `setup.py` and `requirements.txt`
- **Added**: `pyproject.toml` with all project configuration
- **Updated**: Installation and development instructions in README.md
- **Updated**: `tox.ini` to work with uv and modern Python versions (3.10+)

## For Existing Users

If you have an existing installation:

1. Remove your old virtual environment
2. Follow the new installation instructions in README.md using uv

## Quick Start

```bash
# Install uv if you haven't already
curl -LsSf https://astral.sh/uv/install.sh | sh

# Install the project
uv sync

# Run commands
uv run ifexgen --help
uv run ifexgen_dbus --help
uv run ifexconv_protobuf --help

# Run tests
uv run pytest
```

## Development

```bash
# Install with development dependencies
uv sync --extra dev

# Run tests
uv run pytest -v tests
```

The migration maintains full backward compatibility - all the same commands and functionality are available.
