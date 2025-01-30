# get-config

Holds common configuration files for different types of projects.
Also provides a CLI to easily copy config into projects.

## Usage

```sh
get-config python github         # Add GitHub Action templates for Python projects
get-config python ruff           # Insert ruff config into the current pyproject.toml
get-config python git            # Append python items into .gitignore

get-config docker dockerignore   # Add .dockerignore file
get-config docker python         # Get a Dockerfile for build Python applications
get-config docker git            # Append Docker items into .gitignore

get-config --help                # Show help text
```

In general, the format is `get-config <TECH> <CONFIG>`.

A `--force` mode will override existing configuration.

Essentially the CLI just downloads the file from GitHub and places it correctly into the project.

## Install

```sh
# Install into dedicated environment with pipx or uvx
pipx install get-config
uvx install get-config

# Install from source
git clone https://github.com/cooperellidge/explore-your-electricity.git
make .venv
source .venv/bin/activate
```
