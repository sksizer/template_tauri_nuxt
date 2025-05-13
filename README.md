# Tauri + Nuxt.js + TypeScript Template

This template provides a starting point for developing desktop applications using [Tauri](https://tauri.app/), [Nuxt.js](https://nuxt.com/), and [TypeScript](https://www.typescriptlang.org/).

## Project Structure

Unlike typical Tauri templates where frontend code is at the root level, this template uses a peer directory structure:

```
template_tauri_nuxt/
├── src-nuxt/    # Frontend Nuxt.js application
└── src-tauri/   # Rust and Tauri backend code
```

This organization keeps the frontend and backend code cleanly separated while maintaining them at the same level in the project hierarchy.

## Prerequisites

- [Node.js](https://nodejs.org/) (with npm or pnpm)
- [Rust](https://www.rust-lang.org/tools/install)
- [Tauri CLI](https://tauri.app/v1/guides/getting-started/prerequisites)

## Setup Instructions

Before running any Tauri commands, you must install the Node.js dependencies in the frontend directory:

```bash
cd src-nuxt
pnpm install  # or npm install
```

## Development Commands

You can use either cargo or pnpm to run Tauri commands:

### Using cargo

```bash
# Run the app in development mode
cargo tauri dev

# Build the app for production
cargo tauri build
```

### Using pnpm

```bash
# Run the app in development mode
pnpm tauri dev

# Build the app for production
pnpm tauri build
```

## Additional Resources

- [Tauri Documentation](https://tauri.app/v1/guides/)
- [Nuxt.js Documentation](https://nuxt.com/docs)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
