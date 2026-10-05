# Web Application (Frontend)

Next.js-based frontend for the video meetings platform.

## Tech Stack

- **Framework**: Next.js 14.2.15
- **UI Library**: React 18.3.1
- **Language**: TypeScript 5.6.3
- **Linting**: ESLint with Next.js config

## Project Structure

```
web/
├── src/              # Source code
├── public/           # Static assets
├── .next/            # Build output (generated)
├── next.config.js    # Next.js configuration
├── tsconfig.json     # TypeScript configuration
└── package.json      # Dependencies and scripts
```

## Commands

Run these from the `apps/web` directory or use `turbo` from root:

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run clean        # Remove build artifacts
```

## Development

- Development server runs on http://localhost:3000 by default
- Hot reload is enabled in dev mode
- TypeScript strict mode is enabled

## Code Conventions

- Use functional components with hooks
- Place components in `src/components/`
- Place pages in `src/app/` (App Router) or `src/pages/` (Pages Router)
- Use TypeScript for all new files
- Follow the existing project structure when adding new features

## Integration with API

- API backend is in `apps/api`
- Configure API endpoints in environment variables or Next.js config
- Use the appropriate HTTP client (fetch, axios, etc.) for API calls

## Notes for Claude

- This is a Next.js 14 app, which supports both App Router and Pages Router
- Check which routing convention is in use before adding new pages
- Always verify TypeScript types compile before marking work complete
- Run `npm run lint` to check for issues
- Consider responsive design when building UI components

## Documentation Maintenance

**IMPORTANT**: When making architectural changes to the frontend, update this documentation:

- **Changing routing strategy** (App Router ↔ Pages Router): Update project structure and conventions
- **Adding state management** (Redux, Zustand, Context): Document in tech stack and conventions
- **Integrating UI libraries** (Material-UI, Tailwind, etc.): Update tech stack and conventions
- **Adding new npm scripts**: Document them in the commands section
- **Changing build configuration**: Update development section
- **Adding authentication or API integration patterns**: Document in integration section
- **Modifying project structure** (new directories, file organization): Update project structure section

Also update the root `CLAUDE.md` if changes affect the overall monorepo structure or integration between apps.
