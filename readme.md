# swechain

`swechain` is the **core SweChain blockchain implementation**, written in Go.

It provides the main chain logic, commands, and configuration used by the rest
of the SweChain ecosystem.

## Main components (at a glance)

- `cmd/` – command‑line entrypoints (chain binaries and tools).
- `app/` – core application / chain logic.
- `proto/` – protobuf definitions and generated code (`buf.yaml`, `buf.lock`).
- `config.yml` – default configuration.
- `start_swechain.sh` – helper script to start SweChain locally.
- `docs/` and `readme.md` – more detailed documentation.
- `Makefile` – common build / test targets.
- `go.mod`, `go.sum` – Go module files.

## Basic setup

From the repo root:

```bash
go mod tidy
make build      # or: go build ./...
```

To start a local instance, see and run:

```bash
./start_swechain.sh
```

(Use the script and existing `readme.md` in this repo for the exact options and
recommended workflow.)

## Ecosystem

This repo is used together with:

- `lascam-UFU/swechain-mcp-server` – MCP access to SweChain.
- `lascam-UFU/swechain-simulations` – simulations built around SweChain.
- `lascam-UFU/swechain-sdk` – high‑level entry / documentation hub.

For details about commands, configuration, and internals, refer to the existing
`readme.md` and `docs/` in this repository.
