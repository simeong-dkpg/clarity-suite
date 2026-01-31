[project]
name = "clarity-suite"
description = ""
authors = []
telemetry = false
cache_dir = "./.cache"

[contracts.achievement-badge-v5]
path = "contracts/achievement-badge-v5.clar"
clarity_version = 4
epoch = "3.3"

[contracts.auth-registry-v5]
path = "contracts/auth-registry-v5.clar"

# clarity-suite

clarity-suite is a comprehensive suite of Clarity smart contracts and deployment tooling for the Stacks blockchain. It is designed to streamline the development, testing, and deployment of decentralized applications (dApps) on Stacks mainnet, testnet, and devnet environments.

## Features

- **Modular Clarity Contracts:**
	- Includes a wide range of reusable contracts (e.g., achievement badges, registries, counters, storage, multisig helpers, reputation systems, and more).
	- Versioned contract files for easy upgrades and maintenance.

- **Automated Deployment:**
	- Uses [Clarinet](https://docs.hiro.so/clarinet/) for contract checks, deployment planning, and execution.
	- Supports mainnet, testnet, and devnet deployments with environment-specific settings.

- **Configurable Environments:**
	- Environment configuration via TOML files in the `settings/` directory.
	- Easily switch between networks and customize deployment parameters.

- **Testing Suite:**
	- Integrated with modern JavaScript/TypeScript testing frameworks (see `tests/` directory).
	- Supports automated contract testing and validation.

## Project Structure

```
contracts/      # Clarity smart contracts (versioned)
deployments/    # Deployment plans and records
settings/       # Network and deployment configuration files
tests/          # Automated test suites
Clarinet.toml   # Clarinet project configuration
package.json    # Node.js dependencies and scripts
tsconfig.json   # TypeScript configuration
vitest.config.ts# Vitest test runner configuration
```

## Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v16+ recommended)
- [Clarinet](https://docs.hiro.so/clarinet/) (install via `npm install -g @hirosystems/clarinet`)

### Install Dependencies
```bash
npm install
```

### Check Contracts
```bash
clarinet check
```

### Generate Deployment Plan
```bash
clarinet deployment generate --mainnet --low-cost
```

### Apply Deployment Plan
```bash
clarinet deployment apply --mainnet --low-cost
```

### Run Tests
```bash
npm test
```

## Configuration
- Edit network and deployment settings in the `settings/` directory (e.g., `Mainnet.toml`, `Testnet.toml`).
- Update contract logic in the `contracts/` directory.

## Contributing
Pull requests and issues are welcome! Please open an issue to discuss major changes before submitting a PR.

## License
MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgements
- [Hiro Systems](https://www.hiro.so/) for Clarinet and Stacks developer tooling.
- Stacks community contributors.
clarity_version = 4
