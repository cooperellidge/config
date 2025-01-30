# get-conf

Holds common configuration files for different types of projects.
Also provides a CLI to easily copy config into projects.

## Usage

```sh
get-conf python github         # Add GitHub Action templates for Python projects
get-conf python ruff           # Insert ruff config into the current pyproject.toml
get-conf python git            # Append python items into .gitignore

get-conf docker dockerignore   # Add .dockerignore file
get-conf docker python         # Get a Dockerfile for build Python applications
get-conf docker git            # Append Docker items into .gitignore

get-conf --help                # Show help text
```

In general, the format is `get-conf <TECH> <CONFIG>`.

A `--force` mode will override existing configuration.

Essentially the CLI just downloads the file from GitHub and places it correctly into the project.

## Install

```sh
# Install into dedicated environment with pipx or uvx
pipx install get-conf
uvx install get-conf

# Install from source
git clone https://github.com/cooperellidge/get-config.git
make .venv
source .venv/bin/activate
```
