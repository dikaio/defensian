# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build/Test/Lint Commands
- Build: `go build -o defensian ./cmd/defensian`
- Run: `./defensian`
- Test all: `go test ./...`
- Test single: `go test ./path/to/package -run TestName`
- Lint: `golangci-lint run`
- Format: `gofmt -s -w .`

## Code Style Guidelines
- **Structure**: Follow standard Go project layout (`cmd/`, `pkg/`, `internal/`)
- **Imports**: Standard library first, then third-party, then local packages
- **Formatting**: Use `gofmt`, consistent indentation (tabs)
- **Error Handling**: Return errors with context using `fmt.Errorf` or error wrapping
- **Naming**: CamelCase for exported, camelCase for non-exported names
- **Comments**: Document all exported functions following Go convention
- **Dependencies**: Minimize external packages, prefer standard library 
- **Concurrency**: Use goroutines with proper synchronization, avoid data races
- **Testing**: Write comprehensive tests (table-driven where appropriate)