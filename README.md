# Nuxt 3 + TS + Eslint 9 + Prettier - Demo Repository

This is the demo repository for the [Nuxt 3 + TypeScript + Eslint 9 + Prettier](https://dev.to/jeanjavi/nuxt-eslint-9-typescript-prettier-configuration-guide-2024-4h2c) blog post.

## Setup

Make sure to install the dependencies:

```bash
# npm
npm install --legacy-peer-deps
```

### Why `--legacy-peer-deps`?

When using `npm init @eslint/config@latest`, it configures ESLint with the latest compatible dependencies. However, this process can introduce peer dependency conflicts due to the stricter dependency resolution in npm 7 and later. These versions enforce peer dependency rules more strictly, which can lead to conflicts when multiple packages depend on different versions of the same dependency.

The `--legacy-peer-deps` flag tells npm to use the older dependency resolution algorithm used in npm 6, which is more lenient and can bypass these conflicts. This approach helps avoid installation errors and allows the project to proceed without manual dependency resolution.

This issue commonly arises because `@typescript-eslint` and other related packages may require specific versions of ESLint that conflict with other dependencies in the project [Github](https://github.com/eslint/create-config/issues/125).

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build
```

Locally preview production build:

```bash
# npm
npm run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.