This repository is a COPY of the Open Source project [OpenTrader](https://github.com/bludnic/opentrader) but with the following important changes

**Changes:**

- **✨ Build from Source **: Original [OpenTrader](https://github.com/bludnic/opentrader) does not build with the latest npm and pnpm versions. We fixed the compatibility to the [latest available packages](/runtime-environment)
- **📝 Clear Build Instructions provided ** see below
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

