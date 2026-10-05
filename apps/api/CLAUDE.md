# API Application (Backend)

NestJS-based backend API for the video meetings platform.

## Tech Stack

- **Framework**: NestJS 10.4.4
- **Platform**: Express
- **Language**: TypeScript 5.6.3
- **Testing**: Jest 29.7.0 with ts-jest
- **Linting**: ESLint with TypeScript and Prettier

## Project Structure

```
api/
├── src/
│   ├── main.ts           # Application entry point
│   ├── app.module.ts     # Root module
│   └── [features]/       # Feature modules
├── test/                 # E2E tests
├── dist/                 # Build output (generated)
├── nest-cli.json         # Nest CLI configuration
├── tsconfig.json         # TypeScript configuration
└── package.json          # Dependencies and scripts
```

## Commands

Run these from the `apps/api` directory or use `turbo` from root:

```bash
npm run dev          # Start in watch mode
npm run build        # Build for production
npm run start        # Start production server
npm run start:dev    # Start in watch mode (alias)
npm run start:prod   # Start production server (alias)
npm run lint         # Run ESLint with auto-fix
npm run test         # Run unit tests
npm run test:watch   # Run tests in watch mode
npm run test:cov     # Run tests with coverage
npm run clean        # Remove build artifacts
```

## Development

- Development server runs with hot reload enabled
- Default port is typically 3000 (may conflict with Next.js; configure if needed)
- API endpoints follow RESTful conventions
- Use dependency injection for all services

## Code Conventions

- Organize code by feature modules (users, auth, meetings, etc.)
- Each module should have:
  - `*.module.ts` - Module definition
  - `*.controller.ts` - HTTP endpoints
  - `*.service.ts` - Business logic
  - `*.dto.ts` - Data transfer objects
  - `*.entity.ts` - Database entities (if using ORM)
  - `*.spec.ts` - Unit tests
- Use decorators for routing, validation, and dependency injection
- Follow NestJS best practices and conventions

## Testing

- Write unit tests for services and controllers
- Use `@nestjs/testing` for testing utilities
- Mock dependencies in unit tests
- Place e2e tests in the `test/` directory
- Aim for good test coverage on business logic

## Integration with Frontend

- Frontend is in `apps/web`
- Configure CORS appropriately for development and production
- Use DTOs for request/response validation
- Document API endpoints (consider Swagger/OpenAPI)

## Notes for Claude

- This is a NestJS application following the standard module structure
- Always create feature modules with proper dependency injection
- Use class-validator for DTO validation
- Write tests for new services and controllers
- Run `npm run lint` and `npm run test` before marking work complete
- Consider using pipes, guards, and interceptors for cross-cutting concerns
- Database integration (if needed) should use TypeORM, Prisma, or similar

## Documentation Maintenance

**IMPORTANT**: When making architectural changes to the API, update this documentation:

- **Adding new feature modules**: Update the project structure section with module organization
- **Changing the port or server configuration**: Update the development section
- **Adding new npm scripts**: Document them in the commands section
- **Integrating databases or external services**: Update relevant sections and add configuration notes
- **Changing testing setup**: Update the testing section
- **Modifying API structure (GraphQL, WebSockets, etc.)**: Update tech stack and conventions
- **Adding authentication or authorization**: Document in code conventions or create new section

Also update the root `CLAUDE.md` if changes affect the overall monorepo structure or integration between apps.

## Documentation Maintenance

**IMPORTANT**: When making architectural changes to the API, update this documentation:

- **Adding new feature modules**: Update the project structure section with module organization
- **Changing the port or server configuration**: Update the development section
- **Adding new npm scripts**: Document them in the commands section
- **Integrating databases or external services**: Update relevant sections and add configuration notes
- **Changing testing setup**: Update the testing section
- **Modifying API structure (GraphQL, WebSockets, etc.)**: Update tech stack and conventions
- **Adding authentication or authorization**: Document in code conventions or create new section

Also update the root `CLAUDE.md` if changes affect the overall monorepo structure or integration between apps.
