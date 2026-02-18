# Ringier AI Agentic Security

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)

An interactive web application providing a comprehensive, visual guide for securing AI agentic applications using OWASP best practices, NIST AI RMF, MITRE ATLAS, and industry taxonomies.

Developed by Jacques Ackermann.

---

## Features

- **Threat Modeler** -- Drag-and-drop canvas for modeling agentic AI systems with automated MAESTRO-layer threat analysis, STRIDE classification, and exportable reports.
- **NIST AI RMF Mapping** -- Interactive force-directed graph mapping NIST AI Risk Management Framework functions to AISVS security controls.
- **AISVS Controls** -- Full OWASP AI Security Verification Standard (AISVS) with searchable categories, requirements, and implementation guidance.
- **AIVSS Calculator** -- AI Vulnerability Severity Score calculator for quantifying risk in AI/ML systems.
- **Architecture Explorer** -- Visual exploration of common agentic AI architecture patterns (sequential, router, parallel, hierarchical, etc.) with associated threats and mitigations.
- **Threat Catalog** -- Comprehensive catalog of 15 agentic AI threats with attack vectors, impact analysis, and linked mitigations.
- **Security Controls** -- 18 security controls and mitigations with implementation details.
- **OWASP Agentic Top 10** -- Dedicated page for the OWASP Agentic AI Top 10 risks.
- **Cisco AI Security Taxonomy** -- Browsable view of the Cisco AI security taxonomy.
- **Cross-Framework Taxonomy** -- Sankey diagram linking threats across OWASP Agentic, Cisco, and AIVSS frameworks.
- **MITRE ATLAS** -- Tactics, techniques, and case studies from the MITRE ATLAS framework for adversarial ML.
- **Interactive Checklist** -- Security checklist and testing navigator for agentic AI systems.

## Installation Guide

This guide provides detailed, step-by-step instructions to install and run Ringier AI Agentic Security on your local machine.

### Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Node.js** version 20 or higher
- **npm** version 10 or higher
- **Git** for version control
- A code editor (e.g., VS Code, WebStorm, or Sublime Text)

### Step 1: Install Node.js and npm

#### Option A: Using Node Version Manager (nvm) - Recommended

**For macOS/Linux:**

1. Open your terminal

2. Install nvm by running:
   ```sh
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
   ```

3. Close and reopen your terminal, or run:
   ```sh
   source ~/.bashrc  # or ~/.zshrc if using zsh
   ```

4. Install Node.js 20:
   ```sh
   nvm install 20
   nvm use 20
   ```

5. Verify installation:
   ```sh
   node --version  # Should show v20.x.x
   npm --version   # Should show 10.x.x or higher
   ```

**For Windows:**

1. Download nvm-windows from: https://github.com/coreybutler/nvm-windows/releases

2. Run the installer (nvm-setup.exe)

3. Open a new Command Prompt or PowerShell window as Administrator

4. Install Node.js 20:
   ```cmd
   nvm install 20
   nvm use 20
   ```

5. Verify installation:
   ```cmd
   node --version
   npm --version
   ```

#### Option B: Direct Installation

1. Visit https://nodejs.org/

2. Download the LTS version (20.x or higher)

3. Run the installer and follow the installation wizard

4. Verify installation by opening a terminal/command prompt:
   ```sh
   node --version
   npm --version
   ```

### Step 2: Install Git

**For macOS:**
```sh
# Using Homebrew (recommended)
brew install git

# Or download from: https://git-scm.com/download/mac
```

**For Linux (Ubuntu/Debian):**
```sh
sudo apt update
sudo apt install git
```

**For Windows:**
1. Download Git from: https://git-scm.com/download/win
2. Run the installer
3. Use recommended settings during installation

**Verify Git installation:**
```sh
git --version  # Should show git version 2.x.x or higher
```

### Step 3: Clone the Repository

1. Open your terminal or command prompt

2. Navigate to the directory where you want to install the project:
   ```sh
   # Example: Navigate to your Documents folder
   cd ~/Documents  # macOS/Linux
   # or
   cd C:\Users\YourUsername\Documents  # Windows
   ```

3. Clone the repository:
   ```sh
   git clone https://github.com/jacquesackermann/ringier-ai-agentic-security.git
   ```

4. Navigate into the project directory:
   ```sh
   cd ringier-ai-agentic-security
   ```

### Step 4: Install Project Dependencies

1. Install all required npm packages:
   ```sh
   npm install
   ```

   This process may take 2-5 minutes depending on your internet connection.

2. If you encounter any errors during installation, try:
   ```sh
   # Clear npm cache
   npm cache clean --force

   # Try installing again
   npm install
   ```

### Step 5: Start the Development Server

1. Start the Vite development server:
   ```sh
   npm run dev
   ```

2. You should see output similar to:
   ```
   VITE v5.x.x  ready in xxx ms

   ➜  Local:   http://localhost:8080/
   ➜  Network: use --host to expose
   ```

3. Open your web browser and navigate to:
   ```
   http://localhost:8080
   ```

4. The Ringier AI Agentic Security application should now be running!

### Step 6: Verify Installation

To ensure everything is working correctly:

1. **Check the homepage loads** - You should see the Ringier AI Agentic Security landing page

2. **Navigate through different sections:**
   - Threat Modeler
   - AISVS Controls
   - Architecture Explorer
   - Security Controls

3. **Run validation checks:**
   ```sh
   # In a new terminal window (keep the dev server running)
   npm run typecheck  # TypeScript type checking
   npm run lint       # Code linting
   npm run check:data # Data integrity validation
   ```

### Troubleshooting

#### Port Already in Use

If port 8080 is already in use, Vite will automatically try the next available port (8081, 8082, etc.). Check the terminal output for the actual port.

To specify a different port:
```sh
npm run dev -- --port 3000
```

#### Module Not Found Errors

If you see "module not found" errors:
```sh
# Delete node_modules and package-lock.json
rm -rf node_modules package-lock.json  # macOS/Linux
# or
rmdir /s node_modules & del package-lock.json  # Windows

# Reinstall dependencies
npm install
```

#### Permission Errors (macOS/Linux)

If you encounter permission errors:
```sh
# Fix npm permissions
sudo chown -R $USER:$GROUP ~/.npm
sudo chown -R $USER:$GROUP ~/.config
```

#### Windows-Specific Issues

If scripts fail on Windows:
```cmd
# Enable script execution in PowerShell (run as Administrator)
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### Development Workflow

Once installed, here are common commands you'll use:

```sh
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run all validation checks
npm run validate

# Format code
npm run format

# Fix linting issues
npm run lint:fix
```

### Next Steps

- **Explore the Application**: Navigate through all features and components
- **Read the Documentation**: Check out the [Project Structure](#project-structure) section
- **Make Changes**: Start customizing and extending the application
- **Contribute**: See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines

### System Requirements

**Minimum:**
- OS: Windows 10, macOS 10.15, or Linux (Ubuntu 20.04+)
- RAM: 4 GB
- Disk Space: 500 MB for project and dependencies
- Internet Connection: Required for initial setup

**Recommended:**
- RAM: 8 GB or more
- SSD storage for faster development experience
- Modern web browser (Chrome, Firefox, Safari, or Edge - latest version)

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the Vite development server |
| `npm run build` | Production build (outputs to `docs/`) |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |
| `npm run lint:fix` | Run ESLint with auto-fix |
| `npm run typecheck` | TypeScript type checking |
| `npm run format` | Format source files with Prettier |
| `npm run format:check` | Check formatting without writing |
| `npm run check:data` | Validate cross-dataset integrity (threats, controls, AISVS, architectures) |
| `npm run validate` | Run all checks: typecheck, lint, data integrity, and build |

## Project Structure

```
src/
  components/
    architecture/     Architecture explorer (D3 force graph)
    components/       Framework data files (security, architectures, taxonomy)
    home/             Homepage sections
    interactive/      Security checklist and test navigator
    layout/           Header, Footer, Sidebar
    threat-modeler/   Drag-and-drop threat modeling canvas
      edges/          Custom ReactFlow edge types
      engine/         MAESTRO analysis engine and rules
      export/         Report export (PNG, JSON)
      nodes/          Custom ReactFlow node types
      parsers/        Import parsers
    ui/               shadcn/ui primitives
    visual/           Architecture diagrams
  hooks/              Custom React hooks
  lib/                Utilities (analytics, helpers)
  pages/              Route-level page components
scripts/
  check-data-integrity.js   Cross-dataset validation
docs/                       Production build output (GitHub Pages)
public/                     Static assets (favicons, fonts, manifest)
```

## Tech Stack

- [React](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/) -- UI framework
- [Vite](https://vitejs.dev/) -- Build tool and dev server
- [Tailwind CSS](https://tailwindcss.com/) -- Utility-first styling
- [shadcn/ui](https://ui.shadcn.com/) + [Radix UI](https://www.radix-ui.com/) -- Component library
- [D3.js](https://d3js.org/) -- Data visualizations (force graphs, Sankey diagrams)
- [React Flow](https://reactflow.dev/) -- Threat modeler node canvas
- [React Router](https://reactrouter.com/) -- Client-side routing
- [Geist](https://vercel.com/font) -- Typography (Geist Sans + Geist Mono)

## Deployment to GitHub Pages

This project is pre-configured for GitHub Pages deployment with automated CI/CD via GitHub Actions.

### Automatic Deployment

1. **Push your code to GitHub:**
   ```sh
   git add .
   git commit -m "Deploy Ringier AI Agentic Security"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Navigate to **Settings** → **Pages**
   - Under **Source**, select **GitHub Actions**

3. **Automatic deployment:**
   - The GitHub Actions workflow will automatically:
     - Run TypeScript type checking
     - Lint the code
     - Validate data integrity
     - Build the project
     - Deploy to GitHub Pages

4. **Access your site:**
   - Project page: `https://yourusername.github.io/ringier-ai-agentic-security/`
   - Or custom domain: `https://your-custom-domain.com/`

### Manual Deployment

If you prefer manual deployment:

```sh
# Build the project
npm run build

# Commit the build output
git add docs/
git commit -m "Build for production"
git push origin main
```

Then configure GitHub Pages to deploy from the `docs/` folder:
- **Settings** → **Pages** → **Source**: Deploy from a branch
- **Branch**: main, **Folder**: /docs

### Base URL Configuration

**Important:** Update `vite.config.ts` based on your deployment type:

```typescript
// For custom domain or user/org page (username.github.io)
base: "/"

// For project page (username.github.io/repo-name)
base: "/ringier-ai-agentic-security/"
```

### Custom Domain Setup

To use a custom domain:

1. Add a `CNAME` file in the `public/` folder with your domain
2. Configure DNS settings with your domain provider
3. Enable HTTPS in GitHub Pages settings

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a pull request.

## License

This project is licensed under the [Apache License 2.0](LICENSE).

## Contact

- **Author**: Jacques Ackermann
