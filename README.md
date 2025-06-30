# Tenuta Mamie Shopify Theme

A custom Shopify theme for Tenuta Mamie.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (version 20.10.0 or higher)
- **npm** (comes with Node.js)
- **Git** (for version control)

## Installation

### 1. Install Node.js (if not already installed)

If you don't have Node.js 20+ installed, you can install it using Node Version Manager (nvm):

#### Windows:

```bash
# Install NVM for Windows (if not already installed)
winget install CoreyButler.NVMforWindows

# Install Node.js 20
nvm install 20.11.0
nvm use 20.11.0
```

#### macOS/Linux:

```bash
# Install NVM
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# Install Node.js 20
nvm install 20.11.0
nvm use 20.11.0
```

### 2. Install Shopify CLI

Install the Shopify CLI globally:

```bash
npm install -g @shopify/cli
```

**Note:** The `@shopify/theme` package is deprecated and no longer needed as it's bundled with `@shopify/cli`.

### 3. Verify Installation

Check that everything is installed correctly:

```bash
node --version  # Should show v20.x.x
shopify version  # Should show the CLI version
```

## Local Development

### 1. Start Local Development Server

Navigate to your theme directory and start the development server with your store:

```bash
shopify theme dev --store=tenutamamiemarianne.myshopify.com
```

This command will:

- Authenticate you with the specified store (if not already authenticated)
- Upload your local theme to a development theme on your store
- Start a local server (usually at `http://127.0.0.1:9292`)
- Enable live reloading - changes to your theme files will automatically update in the browser

### 2. Make Changes and Preview

- Edit your theme files locally in your code editor
- Save your changes
- The browser preview will automatically update with your changes

### 3. Stop the Development Server

To stop the development server, press `Ctrl + C` in the terminal.

## Project Structure

```
├── assets/          # CSS, JavaScript, and image files
├── config/          # Theme configuration files
├── layout/          # Theme layout templates
├── sections/        # Reusable section templates
├── snippets/        # Reusable code snippets
├── templates/       # Page templates
├── locales/         # Translation files
└── blocks/          # Custom blocks
```

## Common Commands

```bash
# Start development server
shopify theme dev --store=tenutamamiemarianne.myshopify.com

# Deploy theme to production
shopify theme push --store=tenutamamiemarianne.myshopify.com

# Pull theme from production
shopify theme pull --store=tenutamamiemarianne.myshopify.com

# List all themes
shopify theme list --store=tenutamamiemarianne.myshopify.com

# Check theme for issues
shopify theme check
```

## Troubleshooting

### Node.js Version Issues

If you encounter Node.js version warnings, ensure you're using Node.js 20.10.0 or higher:

```bash
node --version
```

### Authentication Issues

If you have trouble with authentication, try:

```bash
shopify logout
shopify theme dev --store=tenutamamiemarianne.myshopify.com
```

### Port Conflicts

If port 9292 is already in use, the CLI will automatically try the next available port.

## Support

For more information about Shopify CLI, visit the [official documentation](https://shopify.dev/docs/themes/tools/cli).
