# Video Meetings Platform

A monorepo project for a video meetings platform built with Next.js frontend and NestJS backend.

## Project Structure

This is a Turborepo monorepo with the following structure:

```
video-meetings/
├── apps/
│   ├── web/          # Next.js frontend application
│   └── api/          # NestJS backend API
└── packages/         # Shared packages (if any)
```

## Tech Stack

### Frontend (apps/web)

- **Framework**: Next.js 14.2.15
- **Runtime**: React 18.3.1
- **Language**: TypeScript 5.6.3
- **Linting**: ESLint with Next.js config

### Backend (apps/api)

- **Framework**: NestJS 10.4.4
- **Runtime**: Node.js with Express
- **Language**: TypeScript 5.6.3
- **Testing**: Jest with ts-jest
- **Linting**: ESLint with TypeScript and Prettier

### Build System

- **Monorepo tool**: Turborepo 2.1.3
- **Package manager**: npm (workspaces)
- **Formatting**: Prettier 3.3.3

## Commands

### Development

```bash
npm run dev          # Run all apps in development mode
```

### Build

```bash
npm run build        # Build all apps
```

### Linting & Formatting

```bash
npm run lint         # Lint all apps
npm run format       # Format all files with Prettier
npm run format:check # Check formatting without writing
```

### Cleanup

```bash
npm run clean        # Clean all build artifacts and node_modules
```

## Requirements

- Node.js >= 18.0.0
- npm >= 9.0.0

## Development Workflow

1. Install dependencies: `npm install`
2. Start development servers: `npm run dev`
3. Frontend will be available at the Next.js default port (typically http://localhost:3000)
4. Backend API will be available at the NestJS default port (typically http://localhost:3000 for NestJS, may need port configuration)

## Code Style

- Use TypeScript for all new code
- Follow ESLint rules configured in each app
- Use Prettier for consistent formatting
- Run `npm run format` before committing

## Notes for Claude

- This is a monorepo; always check which workspace you're working in
- Use `turbo` commands from root to run tasks across apps
- Each app has its own `package.json` and can be worked on independently
- Shared code should go in the `packages/` directory
- Always run linting and formatting before suggesting the work is complete

## Documentation Maintenance

**IMPORTANT**: When making architectural changes to the project, update this documentation:

- **Adding/removing apps or packages**: Update the project structure section and tech stack
- **Changing build tools or monorepo configuration**: Update the build system section and commands
- **Adding new scripts to root package.json**: Document them in the commands section
- **Changing dependencies or frameworks**: Update the tech stack sections
- **Modifying development workflow**: Update the development workflow section
- **Adding environment requirements**: Update the requirements section

After updating this file, also update the relevant `CLAUDE.md` files in affected apps (`apps/web/CLAUDE.md`, `apps/api/CLAUDE.md`) to keep documentation synchronized across the monorepo.

## Documentation Maintenance

**IMPORTANT**: When making architectural changes to the project, update this documentation:

- **Adding/removing apps or packages**: Update the project structure section and tech stack
- **Changing build tools or monorepo configuration**: Update the build system section and commands
- **Adding new scripts to root package.json**: Document them in the commands section
- **Changing dependencies or frameworks**: Update the tech stack sections
- **Modifying development workflow**: Update the development workflow section
- **Adding environment requirements**: Update the requirements section

After updating this file, also update the relevant `CLAUDE.md` files in affected apps (`apps/web/CLAUDE.md`, `apps/api/CLAUDE.md`) to keep documentation synchronized across the monorepo.
