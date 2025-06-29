# Installing Gemini CLI from Local Fork

This document outlines the steps to install the `gemini-cli` package system-wide directly from your local fork, without fetching packages from the internet. This is useful for development or when you need to use a specific version of the CLI from your local workspace.

## Prerequisites

*   Node.js (version 18 or higher) and npm installed on your system.

## Installation Steps

1.  **Navigate to the project root**:
    Open your terminal and navigate to the root directory of your `GeminiCLI` fork.
    ```bash
    cd /Users/Muthu/vscodeInsidersProjects/GeminiCLI/gemini-cli
    ```

2.  **Install project dependencies**:
    Run the following command to install all necessary dependencies for the monorepo, including TypeScript type definitions. This ensures that the build process has all required modules.
    ```bash
    npm install
    ```

3.  **Build and Install the CLI package globally**:
    After the dependencies are installed, navigate into the `packages/cli` directory, build the CLI, and then install it globally. This command compiles the TypeScript source code into JavaScript and then installs the built package system-wide.
    ```bash
    cd packages/cli && npm run build && npm install -g
    ```

## Verification

To verify that `gemini-cli` has been installed correctly and is available system-wide, open a new terminal window (or restart your current one) and run:

```bash
gemini --version
```

You should see the version number of your locally installed `gemini-cli` (e.g., `0.1.8`).
