# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

- **Development**: `yarn dev` - Start Next.js development server
- **Build**: `yarn build` - Build production application
- **Start**: `yarn start` - Start production server
- **Lint**: `yarn lint` - Run ESLint with Next.js configuration

## Package Manager

This project uses **yarn** as the package manager. Always use `yarn` commands instead of npm.

## Code Architecture

This is a Next.js 14.1.0 TypeScript boilerplate with the following key architectural decisions:

### State Management
- **Jotai** for atomic state management
- `JotaiProvider` wraps the entire app in `src/app/layout.tsx`
- Client-side state provider located at `src/app/JotaiProvider.tsx`

### Styling & UI
- **Pretendard font** loaded via CDN in the root layout
- Styled Components compiler enabled in `next.config.mjs`
- Korean locale (`lang="ko"`) set as default

### Date/Time Handling
- **dayjs** configured with timezone plugin
- Default timezone set to `"Asia/Seoul"` in root layout

### File Structure
- `src/app/` - Next.js App Router structure
- `@/*` path alias configured for `./src/*` directory

## Code Standards

### ESLint Configuration
- **Airbnb TypeScript** configuration as base
- **React components must be arrow functions** (`react/function-component-definition`)
- **JSX only in `.tsx` files** (`react/jsx-filename-extension`)
- **Type imports must use `import type`** (`@typescript-eslint/consistent-type-imports`)
- Unused variables generate warnings, not errors
- Various accessibility and React best practices enforced

### TypeScript
- **Strict mode enabled**
- Path aliases configured (`@/*` → `./src/*`)
- Next.js plugin integration for optimal TypeScript experience

### Component Patterns
- All React components should be arrow functions
- Use `interface Props` pattern for component props
- Prefer named exports over default exports where possible
- Type imports should use `import type` syntax

## Architecture Notes

- **React Strict Mode disabled** in Next.js config
- **Styled Components** compiler enabled but no styled-components detected in current codebase
- **Jotai** atoms and state should follow atomic design principles
- **dayjs** timezone handling configured for Seoul timezone by default