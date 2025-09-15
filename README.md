This repository is a COPY of the Open Source project [OpenTrader](https://github.com/bludnic/opentrader) but with the following important changes

**Changes:**

- **✨ Build from Source **: Original [OpenTrader](https://github.com/bludnic/opentrader) does not build with the latest npm and pnpm versions. We fixed the compatibility to the [latest available packages](#runtime-environment)
- **📝 Clear Build Instructions provided ** [see below](#build-instructions)
- **⚙️ Bundling ** Each of the four distinct parts of the system is bundeled into a Single Standalone ES Module

## Runtime Environment

### Node.js
- **Version**: v24.7.0
- **Release**: Current LTS/Latest stable

### Package Managers

#### npm
- **Version**: 11.5.1
- **Bundled with**: Node.js v24.7.0

#### pnpm
- **Version**: 10.16.1
- **Installation**: Standalone package manager


# Build Instructions

## Prerequisites
- Node.js (LTS version recommended)

## Steps

1. **Install pnpm**:
   ```bash
   curl -fsSL https://get.pnpm.io/install.sh | sh -
   source ~/.bashrc
   ```

2. **Navigate to project root and install dependencies**:
   ```bash
   cd crypto
   pnpm install
   ```

3. **Build the application**:
   ```bash
   cd app
   npx tsup
   ```

4. **Test the build** (optional):
   ```bash
   node dist/daemon.mjs
   ```

## Key Notes

- This is a monorepo using pnpm workspaces
- The build creates 4 output files: `main.mjs`, `cli.mjs`, `standalone.mjs`, `daemon.mjs`
- You may see warnings about Node version mismatch (project wants ~22.12, but LTS versions work fine)
- The `pnpm install` at project root installs dependencies for all packages in the workspace
- The project uses TypeScript and builds to ESM format
- Build output is located in `app/dist/` directory